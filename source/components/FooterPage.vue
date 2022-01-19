<template>
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-12 col-lg-3">
                    <h3>About us</h3>
                    <ul>
                        <li>
                            <NuxtLink class="nuxtlink" to="/"
                                >Trang chủ</NuxtLink
                            >
                        </li>
                        <li>
                            <NuxtLink class="nuxtlink" to="/menu"
                                >Menu</NuxtLink
                            >
                        </li>
                        <li>
                            <NuxtLink class="nuxtlink" to="/contact-form"
                                >Liên hệ</NuxtLink
                            >
                        </li>
                    </ul>
                </div>
                <div class="col-12 col-lg-3">
                    <h3>Terms</h3>
                    <ul>
                        <li>
                            <NuxtLink class="nuxtlink" to="/term-of-use"
                                >Điều khoản sử dụng</NuxtLink
                            >
                        </li>
                        <li>
                            <NuxtLink class="nuxtlink" to="/privacy-policy"
                                >Chính sách bảo mật</NuxtLink
                            >
                        </li>
                        <li>
                            <NuxtLink class="nuxtlink" to="/faq">FAQ</NuxtLink>
                        </li>
                    </ul>
                </div>
                <div class="col-12 col-lg-3">
                    <h3>
                        <img src="../assets/images/phone-icon.png" alt="" />
                        Điện thoạt đặt hàng: 1800 6936
                    </h3>
                    <h3>
                        <img src="../assets/images/location-icon.png" alt="" />
                        Liên hệ
                    </h3>
                    <p>
                        Tầng 3-4 Hub Building 195/10E Điện Biên Phủ, P.15 , Quận
                        Bình Thạnh, thành phố Hồ Chí Minh
                    </p>
                </div>
                <div class="col-12 col-lg-3">
                    <img src="../assets/images/facebook-icon.svg" alt="" />
                    <img src="../assets/images/instagram-icon.svg" alt="" />
                </div>
            </div>
        </div>
    </footer>
</template>

<style scoped>
@import '../style/layouts/_footer.scss';
</style>