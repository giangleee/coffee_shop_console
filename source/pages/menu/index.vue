<template>
    <section>
        <div class="about margintop">
            <h2 class="about-title text-center">
                Xuân, hạ, thu, đông, sản phẩm thay đổi theo mùa<br />
                "Kẹo bốn mùa HIBIKA"
            </h2>

            <p class="about-content text-center">
                Đưa sự chuyển mùa tươi đẹp của bốn mùa Nhật Bản vào bánh kẹo
                phương Tây.<br />
                Tại HIBIKA, tất cả đồ ngọt đều có theo mùa.<br />
                Vì vậy mà có một mùi vị và hương thơm đặc trưng của mùa đó.<br />
                Cầu mong có điều gì đó thu hút bạn đến với sự mong manh và cảm
                xúc mà bạn chỉ có thể gặp bây giờ.<br />
                Dòng sản phẩm kẹo HIBIKA thay đổi theo mùa, và chúng tôi chỉ
                chuẩn bị cho họ để vui vào thời điểm đó.<br />
                Trong bốn mùa xuân, hạ, thu, đông, hãy thưởng thức những món đồ
                ngọt theo mùa mang hương vị và màu sắc riêng của từng mùa.<br />
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

                            <h4 class="about-more-title">Đồ ngọt bốn mùa mùa đông</h4>

                            <p class="about-more-date">11 / 17 ～ 2 / 28</p>
                            <p class="about-more-content">
                                Những chiếc bánh có họa tiết hoa trà xứ lạnh nở những bông hoa đỏ tươi vào mùa đông<br />
                                日本の冬の美しい情景をイメージした焼き菓子など<br />
                                Hãy thưởng thức hương vị tinh tế chỉ có trong mùa đông.<br />
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
                                        >Tất cả</span
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
                                        >Cà phê</span
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
                                        >Trà</span
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
                                        >Bánh</span
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
                        <h1 class="title coffee">Cà phê</h1>
                        <div class="row">
                            <div
                                v-for="item in coffee_product.objects"
                                :key="item.id"
                                class="col-4"
                            >
                                <picture>
                                    <img
                                        :src="`../../_nuxt/assets/images${item.link_image}`"
                                        alt=""
                                    />

                                    <NuxtLink
                                        :to="{
                                            path: `/menu/detail/${item.id}`,
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
                        <h1 class="title">Trà</h1>
                        <div class="row">
                            <div
                                v-for="item in tea_product.objects"
                                :key="item.id"
                                class="col-4"
                            >
                                <picture>
                                    <img
                                        :src="`../../_nuxt/assets/images${item.link_image}`"
                                        alt=""
                                    />
                                    <NuxtLink
                                        :to="{
                                            path: `/menu/detail/${item.id}`,
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
                        <h1 class="title">Bánh</h1>
                        <div class="row">
                            <div
                                v-for="item in cake_product.objects"
                                :key="item.id"
                                class="col-4"
                            >
                                <picture>
                                    <img
                                        :src="`../../_nuxt/assets/images${item.link_image}`"
                                        alt=""
                                    />
                                    <NuxtLink
                                        :to="{
                                            path: `/menu/detail/${item.id}`,
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
            title: 'HIBIKA| Menu',
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
            this.tea_product = await this.$axios.$get(
                `/product/category/${this.tea}`
            )
        },
        async getCakeProduct() {
            this.cake_product = await this.$axios.$get(
                `/product/category/${this.cake}`
            )
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