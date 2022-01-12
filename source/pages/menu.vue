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
                                    data-bs-target="#coffee"
                                >
                                    Coffee
                                </button>
                                <div id="coffee" class="collapse">
                                    <ul class="fw-normal pb-1 small">
                                        <li
                                            class="
                                                d-inline-flex
                                                align-items-center
                                                rounded
                                            "
                                        >
                                            Pure Coffee 
                                        </li>
                                    </ul>
                                    <ul class="fw-normal pb-1 small">
                                        <li
                                            class="
                                                d-inline-flex
                                                align-items-center
                                                rounded
                                            "
                                        >
                                            Brew Coffee 
                                        </li>
                                    </ul>
                                </div>
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
                                >
                                    Tea
                                </button>
                                <div id="tea" class="collapse">
                                    <ul class="fw-normal pb-1 small">
                                        <li
                                            class="
                                                d-inline-flex
                                                align-items-center
                                                rounded
                                            "
                                        >
                                            Pure Tea
                                        </li>
                                        <li
                                            class="
                                                d-inline-flex
                                                align-items-center
                                                rounded
                                            "
                                        >
                                            Brew Tea
                                        </li>
                                    </ul>
                                    <ul class="fw-normal pb-1 small">
                                        <li
                                            class="
                                                d-inline-flex
                                                align-items-center
                                                rounded
                                            "
                                        >
                                            Iced Tea 
                                        </li>
                                    </ul>
                                </div>
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
                                >
                                    Cake
                                </button>
                                <div id="cake" class="collapse">
                                    <ul class="fw-normal pb-1 small">
                                        <li
                                            class="
                                                d-inline-flex
                                                align-items-center
                                                rounded
                                            "
                                        >
                                            Pastry
                                        </li>
                                    </ul>
                                    <ul class="fw-normal pb-1 small">
                                        <li
                                            class="
                                                d-inline-flex
                                                align-items-center
                                                rounded
                                            "
                                        >
                                            Tart
                                        </li>
                                    </ul>
                                </div>
                            </li>
                        </ul>
                    </nav>
                </aside>
                <main class="bd-main order-1">
                    <h1 class="title coffee">Coffee</h1>
                    <div class="row">
                        <picture class="col-4">
                            <img
                                src="../assets/images/coffee/coffee_16.jpg"
                                alt=""
                            />
                            <a href="#" class="image-content">Black coffee</a>
                        </picture>
                    </div>
                    <h1 class="title">Tea</h1>
                    <div class="row">
                        <picture class="col-4">
                            <img src="../assets/images/tea/tea_11.jpg" alt="" />
                            <a href="#" class="image-content">Orange lemongrass peach tea</a>
                        </picture>
                    </div>
                    <h1 class="title">Cake</h1>
                    <div class="row">
                        <picture class="col-4">
                            <img src="../assets/images/cake/pyramid-cake.jpg" alt="" />
                            <a href="#" class="image-content">Pyramid cake</a>
                        </picture>
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
}
</script>

<style lang="scss" scoped>
@import '../style/pages/menu.scss';
@import '../style/pages/index/main.scss';
</style>