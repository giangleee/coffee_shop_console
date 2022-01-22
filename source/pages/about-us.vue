<template>
  <main>
        <picture>
            <img src="../assets/images/banner0.png" alt="">
        </picture>

        <div class="infor">
            <h1 class="text-center">Về sở thích của chúng tôi</h1>

        </div>

        <div class="our-fav container">
            <div class="row container-fluid">
                <div class="col-lg-6">
                    <h2 class="text-center">Caffe, sách và tôi</h2>
                    <p>
                        Bước vào phía đặt hàng của quán, gọi cho mình cốc Americano, bất giác thấy quyển sách tôi ngỡ đã
                        đọc chúng từ rất lâu rồi. Có cảm giác deja deja vu đang len lỏi trong tâm trí tôi. Tôi cầm lấy
                        quyển sách đó, ngồi xuống và đắm mình trong tiết trời mưa xuân tháng Giêng.
                    </p>
                    <button type="button" class="btn contact">Contact us</button>
                </div>
                <div class="col-lg-6">
                    <img src="../assets/images/about_us_img.jpg" alt="">
                </div>
            </div>

            <div class="temp2">
                <h1 class="title1">Trời xanh mây trắng</h1>
                <p>Mot doan text nao do</p>
            </div>
            <div class="text-center" style="display: flex; justify-content: flex-end;">
                <div class="temp1">
                    <div class="temp1-text">
                        <h1>Nang vang</h1>
                    <p>mot doan text nao do nua</p>
                    </div>
                </div>
            </div>

        </div>

        <div class="member">
            <div class="infor">
                <h1 class="text-center">Thành viên</h1>

            </div>

            <div class="container-fluid ">
                <div class="row">
                    <div class="col-lg-3 col-md-6 col-sm-12 member-info">
                        <div class="member-img">
                            <picture>
                                <img src="../assets/images/DSC08721.JPG" alt="">
                            </picture>
                        </div>
                        <h3>The name</h3>
                        <p class="border-bt">Chuc vu, thong tin lien quan</p>
                        <p>@email</p>
                    </div>
                    <div class="col-lg-3 col-md-6 col-sm-12 member-info">
                        <div class="member-img">
                            <picture>
                                <img src="../assets/images/DSC08721.JPG" alt="">
                            </picture>
                        </div>
                        <h3>The name</h3>
                        <p class="border-bt">Chuc vu, thong tin lien quan</p>
                        <p>@email</p>
                    </div>
                    <div class="col-lg-3 col-md-6 col-sm-12 member-info">
                        <div class="member-img">
                            <picture>
                                <img src="../assets/images/DSC08721.JPG" alt="">
                            </picture>
                        </div>
                        <h3>The name</h3>
                        <p class="border-bt">Chuc vu, thong tin lien quan</p>
                        <p>@email</p>
                    </div>
                    <div class="col-lg-3 col-md-6 col-sm-12 member-info">
                        <div class="member-img">
                            <picture>
                                <img src="../assets/images/DSC08721.JPG" alt="">
                            </picture>
                        </div>
                        <h3>The name</h3>
                        <p class="border-bt">Chuc vu, thong tin lien quan</p>
                        <p>@email</p>
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
            title: 'HIBIKA| About us',
        }
    },
}
</script>



<style lang="scss" scoped>
@import '../style/pages/about-us.scss';
</style>

