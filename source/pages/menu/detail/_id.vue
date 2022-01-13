<template>
  <div class="detail">
        <main class="detail-item container">
            <div class="row">
                <div class="col-7">
                    <h1>冬霞<span> ふゆがすみ</span></h1>
                    <p class="style-color">ピスタチオ・フレーズ</p>
                    <p class="style-color" style="margin-bottom: 1.875rem;">シチリア ブロンテ産ピスタチオペーストを使用したムースで、苺とフランボワーズのムースと、苺のコンフィチュールを包みました。香り高いピスタチオの風味が広がる贅沢な味わいです。
                    </p>
                    <div class="table-item-detail">
                        <dl>
                            <dt>サイズ</dt>
                            <dd class="text-start">直径60mm × 高さ60mm</dd>
                            <dt>販売期間</dt>
                            <dd class="text-start">2021/11/17～2022/2/28</dd>
                            <dt>価格</dt>
                            <dd class="text-start">￥750（本体価格￥694)</dd>
                            <dt>特定原材料等</dt>
                            <dd class="text-start">小麦,卵,乳成分,アーモンド,ゼラチン,大豆,りんご</dd>
                        </dl>
                    </div>
                </div>
                <div class="col-3">
                    <picture>
                        <img src="../../../assets/images/cake/pyramid-cake.jpg" alt="">
                    </picture>
                </div>
            </div>
        </main>
    
        <section class="feature container">
            <h1 class="text-center">
                冬のケーキ
            </h1>
            <div class="row">
                <div class="col-6 col-lg-3">
                    <picture>
                        <img src="../../../assets/images/cake/cake_9.jpg" alt="">
                        <p class="text-center">some text</p>
                    </picture>
                </div>
                <div class="col-6 col-lg-3">
                    <picture>
                        <img src="../../../assets/images/cake/cake_10.jpg" alt="">
                        <p class="text-center">some text</p>
                    </picture>
                </div>
                <div class="col-6 col-lg-3">
                    <picture>
                        <img src="../../../assets/images/cake/cake_13.jpg" alt="">
                        <p class="text-center">some text</p>
                    </picture>
                </div>
                <div class="col-6 col-lg-3">
                    <picture>
                        <img src="../../../assets/images/cake/cake_7.jpg" alt="">
                        <p class="text-center">some text</p>
                    </picture>
                </div>
                <div class="col-6 col-lg-3">
                    <picture>
                        <img src="../../../assets/images/cake/cake_12.jpg" alt="">
                        <p class="text-center">some text</p>
                    </picture>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'

export default {
    layout: 'AuthPage',
      head(){
    return {
      title: 'HIBIKA|Detail'
      }
  },
}
</script>

<style lang="scss" scoped>
@import '../../../style/pages/menu/detail.scss';
</style>