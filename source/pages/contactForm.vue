<template>
  <body>
    <h1 class="text-center container">CONTACT FORM</h1>
    <div class="container">
      <form class="row g-3" @submit.prevent="submit">
        <div
          class="col-md-6"
          :class="{ 'form-group--error': $v.user.name.$error }"
        >
          <label for="" class="form-label">Name<span> *</span></label>
          <input
            id=""
            v-model.trim="$v.user.name.$model"
            type="text"
            class="form-control background-style"
          />
          <div v-if="$v.user.name.$anyError">
            <div v-if="!$v.user.name.required" class="error" style="color: red">
              Field is required
            </div>
            <div v-if="!$v.user.name.alpha" class="error" style="color: red">
              Must be only text
            </div>
          </div>
        </div>

        <div class="col-md-6">
          <label
            for="inputPassword4"
            class="form-label"
            :class="{ 'form-group--error': $v.user.phone.$error }"
            >Phone <span>*</span></label
          >
          <input
            id="inputPassword4"
            v-model.trim="$v.user.phone.$model"
            type="tel"
            class="form-control background-style"
          />

          <div v-if="$v.user.phone.$anyError">
            <div
              v-if="!$v.user.phone.required"
              class="error"
              style="color: red"
            >
              Field is required
            </div>
            <div v-if="!$v.user.phone.numeric" class="error" style="color: red">
              Phone number is invalid
            </div>

            <div
              v-if="
                (!$v.user.phone.maxLength || !$v.user.phone.minLength) &&
                $v.user.phone.numeric
              "
              class="error"
              style="color: red"
            >
              Must be from 9 to 13 numbers
            </div>
          </div>
        </div>

        <div class="col-md-6">
          <label
            for="inputEmail4"
            class="form-label"
            :class="{ 'form-group--error': $v.user.email.$error }"
            >Email Address <span>*</span></label
          >
          <input
            id="inputEmail4"
            v-model.trim="$v.user.email.$model"
            type="email"
            class="form-control background-style"
            placeholder="Email"
          />
          <div v-if="$v.user.email.$anyError">
            <div
              v-if="!$v.user.email.required"
              class="error"
              style="color: red"
            >
              Field is required
            </div>
            <div
              v-if="!$v.user.email.email"
              class="invald-feedback"
              style="color: red"
            >
              Email is invalid
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <label
            for="inputState"
            class="form-label"
            :class="{ 'form-group--error': $v.user.option.$error }"
            >Choose option below <span>*</span></label
          >
          <select
            id="inputState"
            v-model.trim="$v.user.option.$model"
            class="form-select background-style font-style"
          >
            <option>Option 1</option>
            <option>Option 2</option>
          </select>
          <div v-if="$v.user.option.$anyError">
            <div
              v-if="!$v.user.option.required"
              class="error"
              style="color: red"
            >
              Must be selected
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <label
            for="floatingTextarea2"
            class="form-lable"
            :class="{ 'form-group--error': $v.user.feedback.$error }"
            >Message <span>*</span></label
          >
          <textarea
            id="floatingTextarea2"
            v-model.trim="$v.user.feedback.$model"
            class="form-control background-style"
            rows="5"
          ></textarea>
          <div v-if="$v.user.feedback.$anyError">
            <div
              v-if="!$v.user.feedback.required"
              class="error"
              style="color: red"
            >
              Field is required
            </div>
          </div>
        </div>
        <div class="text-start color-text">
          By submitting this form i accept the <a href="">Privacy Policy</a> of
          this site
        </div>
        <div class="col-12">
          <button type="submit" class="btn btn-primary">Sign in</button>
        </div>
      </form>
    </div>
  </body>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'
import {
  required,
  email,
  numeric,
  minLength,
  maxLength,
  alpha,
} from 'vuelidate/lib/validators'

export default {
  layout: 'AuthPage',

  data() {
    return {
      user: {
        submitStatus: null,
        name: '',
        email: '',
        phone: '',
        feedback: '',
        option: null,
      },
    }
  },

  validations: {
    user: {
      name: {
        required,
        alpha,
        maxLength: maxLength(100),
      },
      email: {
        required,
        email,
      },
      phone: {
        required,
        numeric,
        minLength: minLength(9),
        maxLength: maxLength(13),
      },
      feedback: {
        required,
      },
      option: {
        required,
      },
    },
  },

  methods: {
    async submit() {
      console.log('submit!')
      this.$v.$touch()
      try {
        await this.$axios.$post('http://icanhazip.com', this.user).then((response) => {
          console.log(response)
        })
      } catch (error) {
        console.log(error)
      }
    },
  },
}
</script>

<style lang="scss" scoped >
@import '../style/pages/contactForm.scss';
</style>