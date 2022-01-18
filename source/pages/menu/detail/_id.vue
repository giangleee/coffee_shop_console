<template>
    <div class="detail">
        <main class="detail-item container">
            <div class="row">
                <div class="col-7">
                    <h1>冬霞<span> ふゆがすみ</span></h1>
                    <p class="style-color">{{ mainProduct.title }}</p>
                    <p class="style-color" style="margin-bottom: 1.875rem">
                        {{ mainProduct.description }}
                    </p>
                    <div class="table-item-detail">
                        <dl>
                            <dt>サイズ</dt>
                            <dd class="text-start">直径60mm × 高さ60mm</dd>
                            <dt>販売期間</dt>
                            <dd class="text-start">2021/11/17～2022/2/28</dd>
                            <dt>価格</dt>
                            <dd class="text-start">
                                $ {{ mainProduct.price }}（本体価格￥694)
                            </dd>
                            <dt>特定原材料等</dt>
                            <dd class="text-start">
                                小麦,卵,乳成分,アーモンド,ゼラチン,大豆,りんご
                            </dd>
                        </dl>
                    </div>
                </div>
                <div class="col-3">
                    <picture>
                        <img
                            :src="`../../../_nuxt/assets/images/${mainProduct.link_image}`"
                            alt=""
                        />
                    </picture>
                </div>
            </div>
        </main>

        <section class="feature container">
            <h1 v-if="mainProduct.category_id === coffee" class="text-center" >おすすめのコーヒ</h1>
            <h1 v-if="mainProduct.category_id === tea" class="text-center" >おすすめのお茶</h1>
            <h1 v-if="mainProduct.category_id === cake" class="text-center" >おすすめのケーキ</h1>
            <div class="row">
                <div
                    v-for="item in product.objects"
                    :key="item.id"
                    class="col-6 col-lg-3 item-list"
                >
                    <div class="">
                        <img
                            :src="`../../../_nuxt/assets/images/${item.link_image}`"
                            alt=""
                        />
                        <center>
                          <NuxtLink :to="`../detail/${item.id}`" class="text-center item-link">{{ item.title }}</NuxtLink>
                        </center>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'
export default {
    layout: 'AuthPage',
    data() {
        return {
            images: [],
            product: '',
            temp: '',
            mainProduct: '',
            slideProduct: '',
            coffee: 1,
            tea: 2,
            cake: 3,
        }
    },
    head() {
        return {
            title: 'HIBIKA|Detail',
        }
    },
    created() {
        this.getProduct()
    },
    mounted() {
        this.importAll(require.context('../../../assets/images/', true))
    },
    methods: {
        importAll(r) {
            r.keys().forEach((key) =>
                this.images.push({ pathLong: r(key), pathShort: key })
            )
        },
        async getProduct() {
            this.product = await this.$axios.$get(
                `/product/${this.$route.params.id}`
            )
            this.mainProduct = this.getMainProduct()
        },
        getMainProduct() {
            for (let index = 0; index < this.product.objects.length; index++) {
                const element = this.product.objects[index]
                if (element.id === parseInt(this.$route.params.id)) {
                    return element
                }
            }
        },
    },
}
</script>

<style lang="scss" scoped>
@import '../../../style/pages/menu/detail.scss';
</style>