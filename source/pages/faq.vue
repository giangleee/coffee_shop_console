<template>
    <main>
        <div class="container">
            <div class="row">
                <div class="faq-wrapper">
                    <div class="header">
                        <h1>FAQ - frequently asked question</h1>
                    </div>

                    <!--Part 1-->
                    <div class="fqa-inner">
                        <div class="fqa-item">
                            <div class="fqa-title">
                                <label> 1. FAQ about web </label>
                                <button
                                    href="#info1"
                                    class="btn-plus"
                                    data-bs-toggle="collapse"
                                >
                                    <i class="fas fa-plus 2x faq-plus"></i>
                                </button>
                            </div>

                            <div id="info1" class="content collapse">
                                <p>
                                    Lorem Ipsum is simply dummy text of the
                                    printing and typesetting industry. Lorem
                                    Ipsum has been the industry's standard dummy
                                    text ever since the 1500s, when an unknown
                                    printer took a galley of type and scrambled
                                    it to make a type specimen book. It has
                                    survived not only five centuries, but also
                                    the leap into electronic typesetting,
                                    remaining essentially unchanged.
                                </p>
                            </div>
                        </div>
                    </div>

                    <!--Part 2-->
                    <div class="fqa-inner">
                        <div class="fqa-item">
                            <div class="fqa-title">
                                <label> 2. Why using Japaness </label>
                                <button
                                    href="#info2"
                                    class="btn-plus"
                                    data-bs-toggle="collapse"
                                >
                                    <i class="fas fa-plus 2x faq-plus"></i>
                                </button>
                            </div>

                            <div id="info2" class="content collapse">
                                <p>
                                    Because we want to mainly using in Japan
                                </p>
                            </div>
                        </div>
                    </div>

                    <div class="fqa-inner">
                        <div class="fqa-item">
                            <div class="fqa-title">
                                <label>
                                    3. Why using Japaness
                                </label>
                                <button
                                    href="#info3"
                                    class="btn-plus"
                                    data-bs-toggle="collapse"
                                >
                                    <i class="fas fa-plus 2x faq-plus"></i>
                                </button>
                            </div>

                            <div id="info3" class="content collapse">
                                <p>
                                    Lorem Ipsum is simply dummy text of the
                                    printing and typesetting industry. Lorem
                                    Ipsum has been the industry's standard dummy
                                    text ever since the 1500s, when an unknown
                                    printer took a galley of type and scrambled
                                    it to make a type specimen book. It has
                                    survived not only five centuries, but also
                                    the leap into electronic typesetting,
                                    remaining essentially unchanged.
                                </p>
                            </div>
                        </div>
                    </div>

                    <div class="fqa-inner">
                        <div class="fqa-item">
                            <div class="fqa-title">
                                <label>
                                    4. Why using Japaness
                                </label>
                                <button
                                    href="#info4"
                                    class="btn-plus"
                                    data-bs-toggle="collapse"
                                >
                                    <i class="fas fa-plus 2x faq-plus"></i>
                                </button>
                            </div>

                            <div id="info4" class="content collapse">
                                <p>
                                    Lorem Ipsum is simply dummy text of the
                                    printing and typesetting industry. Lorem
                                    Ipsum has been the industry's standard dummy
                                    text ever since the 1500s, when an unknown
                                    printer took a galley of type and scrambled
                                    it to make a type specimen book. It has
                                    survived not only five centuries, but also
                                    the leap into electronic typesetting,
                                    remaining essentially unchanged.
                                </p>
                            </div>
                        </div>
                    </div>

                    <div class="fqa-inner">
                        <div class="fqa-item">
                            <div class="fqa-title">
                                <label> 5. Why using Japaness </label>
                                <button
                                    href="#info5"
                                    class="btn-plus"
                                    data-bs-toggle="collapse"
                                >
                                    <i class="fas fa-plus 2x faq-plus"></i>
                                </button>
                            </div>

                            <div id="info5" class="content collapse">
                                <p>
                                    Lorem Ipsum is simply dummy text of the
                                    printing and typesetting industry. Lorem
                                    Ipsum has been the industry's standard dummy
                                    text ever since the 1500s, when an unknown
                                    printer took a galley of type and scrambled
                                    it to make a type specimen book. It has
                                    survived not only five centuries, but also
                                    the leap into electronic typesetting,
                                    remaining essentially unchanged.
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'

export default {
    layout: 'AuthPage',
    head() {
        return {
            title: 'HIBIKA|FAQ',
        }
    },
}
</script>



<style lang="scss" scoped>
@import '../style/pages/faq.scss';
</style>