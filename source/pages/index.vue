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

        <div class="about">
            <h2 class="about-title">
                春夏秋冬、季節ごとに装いが移り変わる<br />
                “HIBIKAの四季菓子”
            </h2>

            <p class="about-content">
                にっぽんの美しい四季の移ろいを洋菓子に込めて。<br />
                HIBIKAでは、すべてのお菓子が季節限定です。<br />
                その季節ならではの味わいや香りがあるように。<br />
                今しか出会えない儚さや情緒にこころ惹かれるものがあるように。<br />
                HIBIKAのお菓子も季節ごとにラインナップが入れ替わり、その時期だけのお楽しみとしてご用意しています。<br />
                春夏秋冬、季節ならではの味わいと彩りをちりばめた、折々の四季菓子をご堪能ください。<br />
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
                                src="../assets/images/favorite-drink/bubble_milk.jpg"
                                alt="img-1"
                            />
                        </div>
                        <div class="detail-box">
                            <div class="type">
                                <a href="#">Coffee name</a>
                                <span>Information</span>
                            </div>
                            <p class="price">$5</p>
                        </div>
                    </div>

                    <div class="box">
                        <div class="slide-img">
                            <img
                                src="../assets/images/favorite-drink/iced_coffe.jpg"
                                alt="img-1"
                            />
                        </div>
                        <div class="detail-box">
                            <div class="type">
                                <a href="#">Coffee name</a>
                                <span>Information</span>
                            </div>
                            <p class="price">$5</p>
                        </div>
                    </div>

                    <div class="box">
                        <div class="slide-img">
                            <img
                                src="../assets/images/favorite-drink/iced_honey_coffee.jpg"
                                alt="img-1"
                            />
                        </div>
                        <div class="detail-box">
                            <div class="type">
                                <a href="#">Coffee name</a>
                                <span>Information</span>
                            </div>
                            <p class="price">$5</p>
                        </div>
                    </div>

                    <div class="box">
                        <div class="slide-img">
                            <img
                                src="../assets/images/favorite-drink/iced_latte.jpg"
                                alt="img-1"
                            />
                            <div class="overlay"></div>
                        </div>
                        <div class="detail-box">
                            <div class="type">
                                <a href="#">Coffee name</a>
                                <span>Information</span>
                            </div>
                            <p class="price">$5</p>
                        </div>
                    </div>

                    <div class="box">
                        <div class="slide-img">
                            <img
                                src="../assets/images/favorite-drink/bubble_milk_tea.jpg"
                                alt="img-1"
                            />
                            <div class="overlay"></div>
                        </div>
                        <div class="detail-box">
                            <div class="type">
                                <a href="#">Coffee name</a>
                                <span>Information</span>
                            </div>
                            <p class="price">$5</p>
                        </div>
                    </div>

                    <div class="box">
                        <div class="slide-img">
                            <img
                                src="../assets/images/favorite-drink/iced_coffe_mocha.jpg"
                                alt="img-1"
                            />
                            <div class="overlay"></div>
                        </div>
                        <div class="detail-box">
                            <div class="type">
                                <a href="#">Coffee name</a>
                                <span>Information</span>
                            </div>
                            <p class="price">$5</p>
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
                                            src="../assets/images/story/blog.jpg"
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
                                            src="../assets/images/story/blog.jpg"
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
        }
    },
    head() {
      return {title: 'HIBIKA|Best place to drink'}
    },
    methods: {
        onSlideStart(slide) {
            this.sliding = true
        },
        onSlideEnd(slide) {
            this.sliding = false
        },
    },
}
</script>

<style lang="scss" scoped>
@import '../style/pages/index.scss';

.lSAction > a {
    background-image: url(../assets/images/controls.png) !important;
}

.carousel-control-next-icon {
    background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' fill='%23fff' width='8' height='8' viewBox='0 0 8 8'%3e%3cpath d='M2.75 0l-1.5 1.5L3.75 4l-2.5 2.5L2.75 8l4-4-4-4z'/%3e%3c/svg%3e");
}
</style>
