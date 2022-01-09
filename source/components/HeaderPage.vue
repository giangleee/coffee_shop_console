<template>
    <header>
        <nav class="navbar navbar-light">
            <div class="container-fluid justify-content-center">
                <picture>
                    <img src="../assets/images/logo.svg" alt="" />
                </picture>
                <div class="text-center">
                    <ul class="navbar-nav flex-row mb-2 mb-lg-0">
                        <li class="nav-item">
                            <a
                                class="nav-link active"
                                aria-current="page"
                                href="#"
                                >Top</a
                            >
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#">Menu</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#">News</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#">Story</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#">Contact</a>
                        </li>
                        <li class="nav-item" style="padding-top: 10px">
                            <div class="title-job">
                                <div
                                    class="
                                        btn-group btn-toggle
                                        rounded-pill
                                        btn-switch
                                    "
                                >
                                    <button
                                        class="
                                            active
                                            btn btn-sm btn-check-active
                                            rounded-pill
                                            color-text
                                        "
                                    >
                                        JP
                                    </button>
                                    <button
                                        class="
                                            btn btn-sm btn-check-unactive
                                            rounded-pill
                                            color-text
                                        "
                                    >
                                        EN
                                    </button>
                                </div>
                            </div>
                        </li>
                    </ul>
                </div>
            </div>
            <div>
                <button
                    class="navbar-toggler"
                    type="button"
                    data-bs-toggle="offcanvas"
                    data-bs-target="#offcanvasNavbar"
                    aria-controls="offcanvasNavbar"
                >
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div
                    id="offcanvasNavbar"
                    class="offcanvas offcanvas-end"
                    tabindex="-1"
                    aria-labelledby="offcanvasNavbarLabel"
                >
                    <div class="offcanvas-header">
                        <button
                            type="button"
                            class="btn-close text-reset btn-close-black"
                            data-bs-dismiss="offcanvas"
                            aria-label="Close"
                        ></button>
                    </div>
                    <div class="offcanvas-body">
                        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                            <li class="nav-item">
                                <a
                                    class="nav-link active"
                                    aria-current="page"
                                    href="#"
                                    >Top</a
                                >
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="#">Menu</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="#">News</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="#">Story</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="#">Contact</a>
                            </li>
                            <li class="nav-item">
                                <div class="title-job">
                                    <div
                                        class="
                                            btn-group btn-toggle
                                            rounded-pill
                                            btn-switch
                                        "
                                    >
                                        <button
                                            class="
                                                active
                                                btn btn-sm btn-check-active
                                                rounded-pill
                                                color-text
                                            "
                                        >
                                            JP
                                        </button>
                                        <button
                                            class="
                                                btn btn-sm btn-check-unactive
                                                rounded-pill
                                                color-text
                                            "
                                        >
                                            EN
                                        </button>
                                    </div>
                                </div>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </nav>
    </header>
</template>

<style scoped>
@import '../style/layouts/_header.scss';
</style>