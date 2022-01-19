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
                <NuxtLink class="about-more-link" to="/menu">
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

                            <h4 class="about-more-title">冬の四季菓子</h4>

                            <p class="about-more-date">11 / 17 ～ 2 / 28</p>
                            <p class="about-more-content">
                                冬に真っ赤な花を咲かせる寒椿をモチーフにしたケーキや<br />
                                日本の冬の美しい情景をイメージした焼き菓子など<br />
                                冬季限定の繊細な味わいをお楽しみください。<br />
                            </p>
                        </div>
                    </div>
                </NuxtLink>
            </div>
        </div>

        <div class="favorite">
            <h2 class="title">FAVORITE</h2>
            <section class="slider">
                <infinite-slide-bar
                    duration="35s"
                    direction="reverse"
                    delay="10s"
                    :bar-style="{ padding: '5px 0' }"
                >
                    <div class="box">
                        <div class="slide-img">
                            <img
                                src="../assets/images/coffee/690_690/blend.jpg"
                                alt="img-1"
                            />
                        </div>
                        <div class="detail-box">
                            <div class="type">
                                <a href="#">Blend</a>
                                <span>Information</span>
                            </div>
                            <p class="price">$3</p>
                        </div>
                    </div>

                    <div class="box">
                        <div class="slide-img">
                            <img
                                src="../assets/images/coffee/690_690/capuchino.jpg"
                                alt="img-1"
                            />
                        </div>
                        <div class="detail-box">
                            <div class="type">
                                <a href="#">Capuchino</a>
                                <span>Information</span>
                            </div>
                            <p class="price">$3.20</p>
                        </div>
                    </div>

                    <div class="box">
                        <div class="slide-img">
                            <img
                                src="../assets/images/coffee/690_690/matcha_latte.jpg"
                                alt="img-1"
                            />
                        </div>
                        <div class="detail-box">
                            <div class="type">
                                <a href="#">Matcha latte</a>
                                <span>Information</span>
                            </div>
                            <p class="price">$3.20</p>
                        </div>
                    </div>

                    <div class="box">
                        <div class="slide-img">
                            <img
                                src="../assets/images/coffee/690_690/mocha.jpg"
                                alt="img-1"
                            />
                            <div class="overlay"></div>
                        </div>
                        <div class="detail-box">
                            <div class="type">
                                <a href="#">Mocha</a>
                                <span>Information</span>
                            </div>
                            <p class="price">$2.50</p>
                        </div>
                    </div>

                    <div class="box">
                        <div class="slide-img">
                            <img
                                src="../assets/images/coffee/690_690/presso.jpg"
                                alt="img-1"
                            />
                            <div class="overlay"></div>
                        </div>
                        <div class="detail-box">
                            <div class="type">
                                <a href="#">Presso</a>
                                <span>Information</span>
                            </div>
                            <p class="price">$3.50</p>
                        </div>
                    </div>

                    <div class="box">
                        <div class="slide-img">
                            <img
                                src="../assets/images/coffee/690_690/20191031123921.jpg"
                                alt="img-1"
                            />
                            <div class="overlay"></div>
                        </div>
                        <div class="detail-box">
                            <div class="type">
                                <a href="#">Special</a>
                                <span>Information</span>
                            </div>
                            <p class="price">$3.50</p>
                        </div>
                    </div>
                </infinite-slide-bar>
            </section>
        </div>

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
                                            >お菓子が結ぶ、やさしい時間に。新しい“にっぽんの洋菓子”
                                        </a>
                                    </div>
                                    <p class="article-content">
                                        いにしえより、私たちにっぽん人は
                                        移ろいゆく四季とともに、
                                        その情緒を愉しみながら暮らしてきました。。。
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
                                            >お菓子が結ぶ、やさしい時間に。新しい“にっぽんの洋菓子”
                                        </a>
                                    </div>
                                    <p class="article-content">
                                        いにしえより、私たちにっぽん人は
                                        移ろいゆく四季とともに、
                                        その情緒を愉しみながら暮らしてきました。。。
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
                                            >お菓子が結ぶ、やさしい時間に。新しい“にっぽんの洋菓子”
                                        </a>
                                    </div>
                                    <p class="article-content">
                                        いにしえより、私たちにっぽん人は
                                        移ろいゆく四季とともに、
                                        その情緒を愉しみながら暮らしてきました。。。
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
                                                >お菓子が結ぶ、やさしい時間に。新しい“にっぽんの洋菓子”
                                            </a>
                                        </div>
                                        <p class="article-content">
                                            いにしえより、私たちにっぽん人は
                                            移ろいゆく四季とともに、
                                            その情緒を愉しみながら暮らしてきました。。。
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
                                                >お菓子が結ぶ、やさしい時間に。新しい“にっぽんの洋菓子”
                                            </a>
                                        </div>
                                        <p class="article-content">
                                            いにしえより、私たちにっぽん人は
                                            移ろいゆく四季とともに、
                                            その情緒を愉しみながら暮らしてきました。。。
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
                                                >お菓子が結ぶ、やさしい時間に。新しい“にっぽんの洋菓子”
                                            </a>
                                        </div>
                                        <p class="article-content">
                                            いにしえより、私たちにっぽん人は
                                            移ろいゆく四季とともに、
                                            その情緒を愉しみながら暮らしてきました。。。
                                        </p>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <!--End teaholic-->
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
                                                src="../assets/images/story/blog.jpg"
                                                alt="story-1"
                                            />
                                        </div>
                                        <span class="date">
                                            1/1/2022 <br />
                                        </span>
                                        <div class="article-title">
                                            <a href="#" class=""
                                                >お菓子が結ぶ、やさしい時間に。新しい“にっぽんの洋菓子”
                                            </a>
                                        </div>
                                        <p class="article-content">
                                            いにしえより、私たちにっぽん人は
                                            移ろいゆく四季とともに、
                                            その情緒を愉しみながら暮らしてきました。。。
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
                                        <span class="date">
                                            1/1/2022 <br />
                                        </span>
                                        <div class="article-title">
                                            <a href="#" class=""
                                                >お菓子が結ぶ、やさしい時間に。新しい“にっぽんの洋菓子”
                                            </a>
                                        </div>
                                        <p class="article-content">
                                            いにしえより、私たちにっぽん人は
                                            移ろいゆく四季とともに、
                                            その情緒を愉しみながら暮らしてきました。。。
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
                                        <span class="date">
                                            1/1/2022 <br />
                                        </span>
                                        <div class="article-title">
                                            <a href="#" class=""
                                                >お菓子が結ぶ、やさしい時間に。新しい“にっぽんの洋菓子”
                                            </a>
                                        </div>
                                        <p class="article-content">
                                            いにしえより、私たちにっぽん人は
                                            移ろいゆく四季とともに、
                                            その情緒を愉しみながら暮らしてきました。。。
                                        </p>
                                    </div>
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
        }
    },
    head() {
        return { title: 'HIBIKA|Best place to drink' }
    },
    created() {
        this.getFavoriteProductApi()
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
</style>
