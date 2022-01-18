<template>
    <section>
        <div class="about margintop">
            <h2 class="about-title text-center">
                春夏秋冬、季節ごとに装いが移り変わる<br />
                “HIBIKAの四季菓子”
            </h2>

            <p class="about-content text-center">
                にっぽんの美しい四季の移ろいを洋菓子に込めて。<br />
                HIBIKAでは、すべてのお菓子が季節限定です。<br />
                その季節ならではの味わいや香りがあるように。<br />
                今しか出会えない儚さや情緒にこころ惹かれるものがあるように。<br />
                HIBIKAのお菓子も季節ごとにラインナップが入れ替わり、その時期だけのお楽しみとしてご用意しています。<br />
                春夏秋冬、季節ならではの味わいと彩りをちりばめた、折々の四季菓子をご堪能ください。<br />
            </p>

            <div class="about-more">
                <a href="#" class="about-more-link">
                    <div class="inside">
                        <div class="about-more-img">
                            <img
                                src="../../assets/images/about_more.jpg"
                                alt="about-more"
                            />
                        </div>

                        <div class="about-more-info">
                            <img
                                src="../../assets/images/hibika_logo.svg"
                                alt=""
                                class="about-logo"
                            />

                            <h4 class="about-more-title">冬の四季菓子</h4>

                            <p class="about-more-date">11 / 17 ～ 2 / 28</p>
                            <p class="about-more-content">
                                冬に真っ赤な花を咲かせる寒椿をモチーフにしたケーキや<br />
                                日本の冬の美しい情景をイメージした焼き菓子など<br />
                                冬季限定の繊細な味わいをお楽しみください。<br />
                            </p>
                        </div>
                    </div>
                </a>
            </div>
        </div>
        <section class="menu-item" style="position: relative">
            <div class="container my-md-4 bd-layout">
                <aside class="bd-sidebar">
                    <nav id="bd-docs-nav" class="collapse bd-links sticky-top">
                        <ul class="mb-0 py-3 pt-md-1">
                            <li class="mb-1">
                                <button
                                    class="
                                        btn-d-inline-flex
                                        align-items-center
                                        rounded
                                        btn
                                    "
                                    data-bs-toggle="collapse"
                                    data-bs-target="#all"
                                    @click="getDataMenu('all')"
                                >
                                    <span
                                        :class="{ active: active.all === true }"
                                        >All</span
                                    >
                                </button>
                            </li>
                            <li class="mb-1">
                                <button
                                    class="
                                        btn-d-inline-flex
                                        align-items-center
                                        rounded
                                        btn
                                    "
                                    data-bs-toggle="collapse"
                                    data-bs-target="#coffee"
                                    @click="getDataMenu('coffee')"
                                >
                                    <span
                                        :class="{
                                            active: active.coffee === true,
                                        }"
                                        >Coffee</span
                                    >
                                </button>
                            </li>
                            <li class="mb-1">
                                <button
                                    class="
                                        btn-d-inline-flex
                                        align-items-center
                                        rounded
                                        btn
                                    "
                                    data-bs-toggle="collapse"
                                    data-bs-target="#tea"
                                    @click="getDataMenu('tea')"
                                >
                                    <span
                                        :class="{
                                            active: active.tea === true,
                                        }"
                                        >Tea</span
                                    >
                                </button>
                            </li>
                            <li class="mb-1">
                                <button
                                    class="
                                        btn-d-inline-flex
                                        align-items-center
                                        rounded
                                        btn
                                    "
                                    data-bs-toggle="collapse"
                                    data-bs-target="#cake"
                                    @click="getDataMenu('cake')"
                                >
                                    <span
                                        :class="{
                                            active: active.cake === true,
                                        }"
                                        >Cake</span
                                    >
                                </button>
                            </li>
                        </ul>
                    </nav>
                </aside>
                <main class="bd-main order-1">
                    <div
                        :class="{
                            block: active.coffee === true,
                            display:
                                active.coffee === true ||
                                active.tea === true ||
                                active.cake === true,
                        }"
                    >
                        <h1 class="title coffee">Coffee</h1>
                        <div class="row">
                            <div
                                v-for="item in coffee_product.objects"
                                :key="item.id"
                                class="col-4"
                            >
                                <picture>
                                    <img
                                        :src="`../../_nuxt/assets/images/${item.link_image}`"
                                        alt=""
                                    />

                                    <NuxtLink
                                        :to="{
                                            path: `detail/${item.id}`,
                                        }"
                                        class="image-content text-center"
                                        >{{ item.title }}</NuxtLink
                                    >
                                </picture>
                            </div>
                        </div>
                    </div>

                    <div
                        :class="{
                            block: active.tea === true,
                            display:
                                active.coffee === true ||
                                active.tea === true ||
                                active.cake === true,
                        }"
                    >
                        <h1 class="title">Tea</h1>
                        <div class="row">
                            <div
                                v-for="item in tea_product.objects"
                                :key="item.id"
                                class="col-4"
                            >
                                <picture>
                                    <img
                                        :src="`../../_nuxt/assets/images/${item.link_image}`"
                                        alt=""
                                    />
                                    <NuxtLink
                                        :to="{
                                            path: `detail/${item.id}`,
                                            params: { tea_product },
                                        }"
                                        class="image-content text-center"
                                        >{{ item.title }}</NuxtLink
                                    >
                                </picture>
                            </div>
                        </div>
                    </div>

                    <div
                        :class="{
                            block: active.cake === true,
                            display:
                                active.coffee === true ||
                                active.tea === true ||
                                active.cake === true,
                        }"
                    >
                        <h1 class="title">Cake</h1>
                        <div class="row">
                            <div
                                v-for="item in cake_product.objects"
                                :key="item.id"
                                class="col-4"
                            >
                                <picture>
                                    <img
                                        :src="`../../_nuxt/assets/images/${item.link_image}`"
                                        alt=""
                                    />
                                    <NuxtLink
                                        :to="{
                                            path: `detail/${item.id}`,
                                            params: { cake_product },
                                        }"
                                        class="image-content text-center"
                                        >{{ item.title }}</NuxtLink
                                    >
                                </picture>
                            </div>
                        </div>
                    </div>
                </main>
            </div>
        </section>
    </section>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'
export default {
    layout: 'AuthPage',
    data() {
        return {
            coffee_product: '',
            tea_product: '',
            cake_product: '',
            all: 0,
            coffee: 1,
            tea: 2,
            cake: 3,
            images: [],
            active: { all: true, coffee: false, tea: false, cake: false },
        }
    },
    head() {
        return {
            title: 'HIBIKA|Menu',
        }
    },
    created() {
        this.getCoffeeProduct()
        this.getTeaProduct()
        this.getCakeProduct()
    },
    mounted() {
        this.importAll(require.context('../../assets/images/', true))
    },
    methods: {
        async getCoffeeProduct() {
            this.coffee_product = await this.$axios.$get(
                `/product/category/${this.coffee}`
            )
        },
        async getTeaProduct() {
            this.tea_product = await this.$axios.$get(`/product/category/${this.tea}`)
        },
        async getCakeProduct() {
            this.cake_product = await this.$axios.$get(`/product/category/${this.cake}`)
        },
        importAll(r) {
            r.keys().forEach((key) =>
                this.images.push({ pathLong: r(key), pathShort: key })
            )
        },
        getDataMenu(string) {
            if (string === 'all') {
                this.active.all = true
                this.active.coffee = false
                this.active.tea = false
                this.active.cake = false
            }
            if (string === 'coffee') {
                this.active.all = false
                this.active.coffee = true
                this.active.tea = false
                this.active.cake = false
            }
            if (string === 'tea') {
                this.active.all = false
                this.active.coffee = false
                this.active.tea = true
                this.active.cake = false
            }
            if (string === 'cake') {
                this.active.all = false
                this.active.coffee = false
                this.active.tea = false
                this.active.cake = true
            }
        },
    },
}
</script>

<style lang="scss" scoped>
@import '../../style/pages/menu.scss';
@import '../../style/pages/index/main.scss';
.active:before {
    display: inline;
}
.display {
    display: none;
}
.block {
    display: block;
}
</style>