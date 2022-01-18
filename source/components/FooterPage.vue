<template>
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-12 col-lg-3">
                    <h3>About us</h3>
                    <ul>
                        <li><NuxtLink class="nuxtlink" to="/">Home</NuxtLink></li>
                        <li><NuxtLink class="nuxtlink" to="../menu">Menu</NuxtLink></li>
                        <li><NuxtLink class="nuxtlink" to="../contact-form">Contact form</NuxtLink></li>
                    </ul>
                </div>
                <div class="col-12 col-lg-3">
                    <h3>Terms</h3>
                    <ul>
                        <li>
                            <NuxtLink class="nuxtlink" to="../term-of-use">Terms of Use</NuxtLink>
                          </li>
                        <li>
                          <NuxtLink class="nuxtlink" to="../privacy-policy">Privacy Policy</NuxtLink>
                        </li>
                        <li>
                          <NuxtLink class="nuxtlink" to="../faq">FAQ</NuxtLink>
                        </li>
                    </ul>
                </div>
                <div class="col-12 col-lg-3">
                    <h3>
                        <img src="../assets/images/phone-icon.png" alt="" />
                        Order number: 1800 6936
                    </h3>
                    <h3>
                        <img src="../assets/images/location-icon.png" alt="" />
                        Contact
                    </h3>
                    <p>
                        3rd-4th floor Hub Building 195/10E Dien Bien Phu, P.15 ,
                        Binh Thanh district, Ho Chi Minh city
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