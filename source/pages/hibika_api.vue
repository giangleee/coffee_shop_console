<template>
    <div id="main">
        <div class="banner">
            <b-carousel
                id="carousel-1"
                v-model="slide"
                class="carousel slide"
                :interval="4000"
                controls
                indicators
                @sliding-start="onSlideStart"
                @sliding-end="onSlideEnd"
            >
                <b-carousel-slide
                    img-src="../assets/images/mv_00.jpg"
                ></b-carousel-slide>

                <b-carousel-slide
                    img-src="../assets/images/mv_01.jpg"
                ></b-carousel-slide>

                <b-carousel-slide
                    img-src="../assets/images/mv_03.jpg"
                ></b-carousel-slide>
            </b-carousel>
        </div>

        <div id="news" class="about">
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
                    <div class="about-more-inside">
                        <div class="about-more-img">
                            <img
                                src="../assets/images/about_more.jpg"
                                alt="about-more"
                            />
                        </div>

                        <div class="about-more-info">
                            <img
                                src="../assets/images/hibika_logo.svg"
                                alt=""
                                class="about-logo"
                            />

                            <h4 class="about-more-title">
                                Đồ ngọt bốn mùa mùa đông
                            </h4>

                            <p class="about-more-date">11 / 17 ～ 2 / 28</p>
                            <p class="about-more-content">
                                Những chiếc bánh có họa tiết hoa trà xứ lạnh nở
                                những bông hoa đỏ tươi vào mùa đông<br />
                                日本の冬の美しい情景をイメージした焼き菓子など<br />
                                Hãy thưởng thức hương vị tinh tế chỉ có trong
                                mùa đông.<br />
                            </p>
                        </div>
                    </div>
                </a>
            </div>
        </div>

        <h2 class="title">FAVORITE</h2>

        <infinite-slide-bar
            duration="35s"
            direction="reverse"
            :bar-style="{ padding: '5px 0' }"
        >
            <div class="loop">
                <div v-for="item in favorite.objects" :key="item.id">
                    <div class="box">
                        <div class="slide-img">
                            <img
                                :src="`../_nuxt/assets/images${item.link_image}`"
                                alt="img-1"
                            />
                        </div>
                        <div class="detail-box">
                            <div class="type">
                                <a href="#">{{ item.title }}</a>
                                <span>{{ item.description }}</span>
                            </div>
                            <p class="price">$ {{ item.price }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </infinite-slide-bar>

        <div class="story frame-margin">
            <h5 class="title text-center">STORIES</h5>

            <div class="story-content container-fluid">
                <div class="coffeeholic">
                    <h3 class="story-title"><a href="">Coffeeholic</a></h3>
                    <!--Coffee holic-->
                    <div class="coffeeholic-box">
                        <div class="row coffeeholic-section">
                            <div class="col-none-12 col-md-6 col-lg-4">
                                <div class="story-box">
                                    <div class="story-img">
                                        <img
                                            src="../assets/images/story/story1.png"
                                            alt="story-1"
                                        />
                                    </div>
                                    <span class="date"> 1/1/2022 <br /> </span>
                                    <div class="article-title">
                                        <a href="#" class=""
                                            >Đối với một thời gian nhẹ nhàng khi
                                            đồ ngọt được buộc. "Bánh kẹo Nhật
                                            Bản" mới
                                        </a>
                                    </div>
                                    <p class="article-content">
                                        Từ xa xưa, người Nhật chúng ta Với sự
                                        thay đổi bốn mùa Tôi đã sống khi tận
                                        hưởng cảm xúc đó. .. ..
                                    </p>
                                </div>
                            </div>

                            <div class="col-none-12 col-md-6 col-lg-4">
                                <div class="story-box">
                                    <div class="story-img">
                                        <img
                                            src="../assets/images/story/story1.png"
                                            alt="story-1"
                                        />
                                    </div>
                                    <span class="date"> 1/1/2022 <br /> </span>
                                    <div class="article-title">
                                        <a href="#" class=""
                                            >Đối với một thời gian nhẹ nhàng khi
                                            đồ ngọt được buộc. "Bánh kẹo Nhật
                                            Bản" mới
                                        </a>
                                    </div>
                                    <p class="article-content">
                                        Từ xa xưa, người Nhật chúng ta Với sự
                                        thay đổi bốn mùa Tôi đã sống khi tận
                                        hưởng cảm xúc đó. .. ..
                                    </p>
                                </div>
                            </div>

                            <div class="col-none-12 col-md-6 col-lg-4">
                                <div class="story-box">
                                    <div class="story-img">
                                        <img
                                            src="../assets/images/story/story1.png"
                                            alt="story-1"
                                        />
                                    </div>
                                    <span class="date"> 1/1/2022 <br /> </span>
                                    <div class="article-title">
                                        <a href="#" class=""
                                            >Đối với một thời gian nhẹ nhàng khi
                                            đồ ngọt được buộc. "Bánh kẹo Nhật
                                            Bản" mới
                                        </a>
                                    </div>
                                    <p class="article-content">
                                        Từ xa xưa, người Nhật chúng ta Với sự
                                        thay đổi bốn mùa Tôi đã sống khi tận
                                        hưởng cảm xúc đó. .. ..
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>
                    <!--End Coffee holic-->
                </div>

                <div class="teaholic">
                    <div class="coffeeholic">
                        <h3 class="story-title-2"><a href="">Teaholic</a></h3>

                        <!--Tea holic-->
                        <div class="coffeeholic-box">
                            <div class="row coffeeholic-section">
                                <div class="col-none-12 col-md-6 col-lg-4">
                                    <div class="story-box">
                                        <div class="story-img">
                                            <img
                                                src="../assets/images/story/teaholic.jpg"
                                                alt="story-1"
                                            />
                                        </div>
                                        <span class="date">
                                            1/1/2022 <br />
                                        </span>
                                        <div class="article-title">
                                            <a href="#" class=""
                                                >Đối với một thời gian nhẹ nhàng
                                                khi đồ ngọt được buộc. "Bánh kẹo
                                                Nhật Bản" mới
                                            </a>
                                        </div>
                                        <p class="article-content">
                                            Từ xa xưa, người Nhật chúng ta Với
                                            sự thay đổi bốn mùa Tôi đã sống khi
                                            tận hưởng cảm xúc đó. .. ..
                                        </p>
                                    </div>
                                </div>

                                <div class="col-none-12 col-md-6 col-lg-4">
                                    <div class="story-box">
                                        <div class="story-img">
                                            <img
                                                src="../assets/images/story/teaholic.jpg"
                                                alt="story-1"
                                            />
                                        </div>
                                        <span class="date">
                                            1/1/2022 <br />
                                        </span>
                                        <div class="article-title">
                                            <a href="#" class=""
                                                >Đối với một thời gian nhẹ nhàng
                                                khi đồ ngọt được buộc. "Bánh kẹo
                                                Nhật Bản" mới
                                            </a>
                                        </div>
                                        <p class="article-content">
                                            Từ xa xưa, người Nhật chúng ta Với
                                            sự thay đổi bốn mùa Tôi đã sống khi
                                            tận hưởng cảm xúc đó. .. ..
                                        </p>
                                    </div>
                                </div>

                                <div class="col-none-12 col-md-6 col-lg-4">
                                    <div class="story-box">
                                        <div class="story-img">
                                            <img
                                                src="../assets/images/story/teaholic.jpg"
                                                alt="story-1"
                                            />
                                        </div>
                                        <span class="date">
                                            1/1/2022 <br />
                                        </span>
                                        <div class="article-title">
                                            <a href="#" class=""
                                                >Đối với một thời gian nhẹ nhàng
                                                khi đồ ngọt được buộc. "Bánh kẹo
                                                Nhật Bản" mới
                                            </a>
                                        </div>
                                        <p class="article-content">
                                            Từ xa xưa, người Nhật chúng ta Với
                                            sự thay đổi bốn mùa Tôi đã sống khi
                                            tận hưởng cảm xúc đó. .. ..
                                        </p>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <!--End teaholic-->
                    </div>
                </div>
            </div>

            <div class="blog">
                <div class="coffeeholic">
                    <h3 class="story-title-2"><a href="">Blog</a></h3>
                    <div class="coffeeholic-box">
                        <div class="row coffeeholic-section">
                            <div class="col-none-12 col-md-6 col-lg-4">
                                <div class="story-box">
                                    <div class="story-img">
                                        <img
                                            src="../assets/images/sensei.png"
                                            alt="story-1"
                                        />
                                    </div>
                                    <span class="date">
                                        01/01/2022 <br />
                                    </span>
                                    <div class="article-title">
                                        <a href="#" class=""
                                            >Một giáo viên đã truyền cảm hứng
                                            cho chúng tôi tạo ra trang web này.
                                        </a>
                                    </div>
                                    <p class="article-content">
                                        Chúng tôi tạo ra trang web này với tình
                                        yêu dành cho cùng một loại cà phê. Chúng
                                        tôi hy vọng trang web này sẽ được những
                                        người yêu thích cà phê sử dụng trong
                                        tương lai.
                                    </p>
                                </div>
                            </div>

                            <div class="col-none-12 col-md-6 col-lg-4">
                                <div class="story-box">
                                    <div class="story-img text-center">
                                        <img
                                            src="../assets/images/sensei_2.jpg"
                                            alt="story-1"
                                        />
                                    </div>
                                    <span class="date"> 1/1/2022 <br /> </span>
                                    <div class="article-title">
                                        <a href="#" class=""
                                            >Thầy Phương-người truyền cảm hứng
                                            cho chúng tôi là người như nào?
                                        </a>
                                    </div>
                                    <p class="article-content">
                                        Là một giáo viên bộ môm Hệ thống thông
                                        tin tại SOICT, với niềm đam mê cà phê
                                        bất diệt, chúng tôi hi vọng thầy chính
                                        là hình mãu tương lai của chúng tôi:
                                        người đồng nghiệp kính mến và người thầy
                                        mẫu mực
                                    </p>
                                </div>
                            </div>

                            <div class="col-none-12 col-md-6 col-lg-4">
                                <div class="story-box">
                                    <div class="story-img">
                                        <img
                                            src="../assets/images/story/blog.jpg"
                                            alt="story-1"
                                        />
                                    </div>
                                    <span class="date"> 1/1/2022 <br /> </span>
                                    <div class="article-title">
                                        <a href="#" class=""
                                            >Đối với một thời gian nhẹ nhàng khi
                                            đồ ngọt được buộc. "Bánh kẹo Nhật
                                            Bản" mới
                                        </a>
                                    </div>
                                    <p class="article-content">
                                        Từ xa xưa, người Nhật chúng ta Với sự
                                        thay đổi bốn mùa Tôi đã sống khi tận
                                        hưởng cảm xúc đó. .. ..
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'
export default {
    layout: 'AuthPage',
    data() {
        return {
            slide: 0,
            sliding: null,
            favorite: '',
            images: [],
        }
    },
    head() {
        return { title: 'HIBIKA|Best place to drink' }
    },
    created() {
        this.getFavoriteProductApi()
    },
    mounted() {
        this.importAll(require.context('../assets/images/', true))
    },
    methods: {
        onSlideStart(slide) {
            this.sliding = true
        },
        onSlideEnd(slide) {
            this.sliding = false
        },
        async getFavoriteProductApi() {
            this.favorite = await this.$axios.$get('/product/favorite')
        },
        importAll(r) {
            r.keys().forEach((key) =>
                this.images.push({ pathLong: r(key), pathShort: key })
            )
        },
    },
}
</script>

<style lang="scss" scoped>
@import '../style/pages/index.scss';
.lSAction > a {
    background-image: url(../assets/images/controls.png) !important;
}
.loop {
    display: flex;
    justify-content: center;
}
#main .about {
    font-family: '游明朝体', 'Yu Mincho', YuMincho, 'ヒラギノ明朝 Pro',
        'Hiragino Mincho Pro', 'MS P明朝', 'MS PMincho', serif !important;
}

.story-img img {
    max-width: 546px !important;
    max-height: 415px !important;
}
</style>