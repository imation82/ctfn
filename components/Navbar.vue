<template>
    <section class="navbar-background">
        <nav id="nav" class="navbar-items">
            <b-container>
                <main class="main-content">
                    <b-img src="../assets/images/logo.png" alt="Logo" @click="$router.push('/')" class="logo" fluid></b-img>
                    <div class="navbar-links">
                        <MenuLinks />
                    </div>
                    <div @click="iconShow = !iconShow" class="navbar-menu-icon">
                        <div class="menu-icon-bar" :class="iconShow ? 'line1' : ''"></div>
                        <div class="menu-icon-bar" :class="iconShow ? 'line2' : ''"></div>
                        <div class="menu-icon-bar" :class="iconShow ? 'line3' : ''"></div>
                    </div>
                    <transition name="slide">
                        <div v-if="iconShow" class="navbar-links-mobileView">
                            <ul class="mobileView-list">
                                <li @click="iconShow = !iconShow" class="mobileView-items"><a href="/#about">About</a>
                                </li>
                                <li @click="iconShow = !iconShow" class="mobileView-items">
                                    <a href="/#products">Products</a>
                                </li>
                                <li @click="iconShow = !iconShow" class="mobileView-items">
                                    <a href="/team">Team</a>
                                </li>
                                <li @click="iconShow = !iconShow" class="mobileView-items">
                                    <a href="/#contact">Contact</a>
                                </li>
                                <li @click="iconShow = !iconShow" class="mobileView-items">
                                    <a href="/#request-trial">Request Trial</a>
                                </li>                                                                
                                <li @click="iconShow = !iconShow" class="mobileView-items">
                                    <a href="">Subscriber Portal</a>
                                </li>                                                               
                            </ul>
                        </div>
                    </transition>
                    <div class="subscribeButton">
                        <a class="contact-button-link">
                            <b-btn class="subscribeBtn" href="">Subscriber Portal</b-btn>
                        </a>                                           
                    </div>
                </main>
            </b-container>
        </nav>
    </section>
</template>
<script>

export default {
    components: {
        MenuLinks: () => import("@/components/MenuLinks.vue"),
    },
    data() {
        return {
            active: false,
            iconShow: false,
        };
    },
    mounted() {
        window.document.onscroll = () => {
            let navBar = document.getElementById("nav");
            if (window.scrollY > navBar.offsetTop) {
                this.active = true;
            } else {
                this.active = false;
            }
        };
    }
};
</script>
<style scoped>
@import "../assets/styles/navbar.css";

.slide-enter-active,
.slide-leave-active {
    transition: transform 0.8s ease;
}

.slide-enter,
.slide-leave-to {
    transform: translateX(-100%);
    transition: all 0.5s ease-in 0s;
}

.is_sticky {
    padding: 10px 0px;
    position: fixed;
    top: 0;
    right: 0;
    left: 0;
    z-index: 20;
    width: 100%;
    background: #12a8db;
}

@media screen and (max-width: 575px) {
    .is_sticky {
        padding: 10px 0;
    }
}
</style>
  