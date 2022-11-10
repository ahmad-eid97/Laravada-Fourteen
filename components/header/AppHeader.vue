<template>
    <header :class="!topOfPage ? 'onScroll' : ''" class="header header-style-2 clearfix">
        <div class="row m-0 w-100">
            <b-navbar toggleable="lg">
                <b-navbar-brand href="#">
                    <img src="/assets/logo2.png" alt="" style="width: 200px; margin: 15px 0">
                </b-navbar-brand>

                <b-navbar-toggle target="navbar-toggle-collapse">
                    <template #default="{ expanded }">
                        <span class="menu-trigger" :class="expanded ? 'active' : ''" id="menu03">
                            <p></p>
                            <p></p>
                            <p></p>
                        </span>
                    </template>
                </b-navbar-toggle>

                <b-collapse id="navbar-toggle-collapse" class="ml-auto justify-content-end" is-nav>
                    <b-navbar-nav class="align-items-center">
                        <b-nav-item class="active" href="/">Home</b-nav-item>
                        <b-nav-item href="#">Services</b-nav-item>
                        <b-nav-item href="#">Company</b-nav-item>
                        <b-nav-item href="#">Our Benefits</b-nav-item>
                        <b-nav-item href="#">Free Consultation</b-nav-item>
                        <b-nav-item href="#">Our Team</b-nav-item>
                        <b-nav-item href="#">Our Team</b-nav-item>
                        <div>
                            <lang-switch></lang-switch>
                        </div>
                        <a href="#" @click="side = !side" class="btn">
                            <font-awesome-icon icon="fa-solid fa-bag-shopping" />
                            <span class="d-lg-none d-block">Side Bar</span>
                        </a>
                    </b-navbar-nav>
                </b-collapse>
            </b-navbar>
        </div>
    </header>
</template>

<script>
import langSwitch from "../langSwitch/langSwitch.vue"

export default {
    name: 'AppHeader',
    components: {
        langSwitch
    },
    data() {
        return {
            topOfPage: true
        }
    },
    beforeMount() {
        window.addEventListener('scroll', this.handleScroll)
    },
    mounted() {
    },
    methods: {
        handleScroll(){
            if(window.pageYOffset>30){
                if(this.topOfPage) this.topOfPage = false
            } else {
                if(!this.topOfPage) this.topOfPage = true
            }
        }
    }
}
</script>
<style lang="scss">
    header {
        position: fixed;
        left: 0;
        right: 0;
        z-index: 10;
        background: transparent;
    }
    .onScroll {
        position: fixed;
        width: 100%;
        /* height: 70px; */
        display: flex;
        align-items: center;
        transition: all .2s ease-in-out;
        box-shadow: 0 0 10px #aaa;
        background-color: #fff;
        top: 0;
        z-index: 10;
        background-image: none;
        * {
            color: #000 !important;
        }
    }
    @include xs {
        .navbar {
            padding: 10px 20px !important;
        }
        .onScroll .navbar {
            padding: 10px 20px !important;
        }
    }
    .onScroll .top-bar {
        overflow: hidden;
        height: 0px;
        padding: 0px;
    }
    .onScroll .social-icon {
        display: none;
    }
    nav {
        padding: 20px 60px 0 !important;
    }
    .onScroll nav {
        padding: 0 60px 0 !important;
    }
    .navbar-brand {
        width: 180px;
        transition: all 0.3s linear;

    }
    .onScroll .navbar-brand {
        width: 140px;

    }
    .navbar .nav-item {
        margin: 0 16px;
        position: relative;
        padding: 5px 0;
    }
    .navbar .nav-item .nav-link {
        background-clip: border-box;
        background-color: rgba(0, 0, 0, 0);
        color: rgb(255, 255, 255);
        display: block;
        font-size: 16px;
        font-weight: 700;
        line-height: 20px;
        padding: 0;
    }
    .onScroll .navbar .nav-item .nav-link {
        color: rgb(0, 0, 0);
    }
    .onScroll .nav-item.active::after, .onScroll .nav-item:hover::after  {
        background-color: rgb(0, 0, 0);
    }

    .nav-item.active::after, .nav-item:hover::after {
        background-color: #fff;
        left: 0px;
        right: 0px;
    }
    .nav-item::after {
        content: " ";
        position: absolute;
        bottom: 0;
        left: 0px;
        right: 100%;
        height: 2px;
        transition: all .3s cubic-bezier(.42,.01,.58,1);
        z-index: 999999998;
        background-color: transparent;
    }
    .navbar .btn {
        font-size: 26px;
    }
    .navbar .btn:hover {
        color: rgb(0, 206, 200);
        border-color: transparent;
    }
    .navbar-toggler {
        border: 1px solid var(--main-color);
        outline: none;
        box-shadow: none !important;
    }
    .menu-trigger p {
        width: 30px;
        height: 5px;
        background: var(--main-color);
        margin: 0 0 2px;
    }
    .navbar .btn:hover {
        color: rgb(210, 52, 48);
        background-color: var(--main-color);
    }
    
    .side-bar {
        width: 0;
        position: fixed;
        overflow: hidden;
        top: 0;
        bottom: 0;
        right: 0;
        background-color: rgba(243, 245, 246, 0.95);
        z-index: 9999;
        transition: all .4s ease;
        padding: 0;
    }
    .side-bar.opend {
        width: 100%;
        background: rgba(0, 0, 0, 0.25);
    }
    .side-bar .content-wrapper {
        padding: 60px 30px;
        position: relative;
        overflow-x: hidden;
        overflow-y: auto;
        height: 100%;
        scrollbar-width: none;
        width: 300px;
        float: right;
        box-shadow: 0 0 5px 0 rgba(0,0,0,.15);
        background: #fff;
    }
    .side-bar .content-wrapper .close-btn {
        position: absolute;
        top: 20px;
        left: auto;
        right: 20px;
        color: rgb(97, 106, 125);
        font-size: 20px;
        cursor: pointer;
    }
    .side-bar .content-wrapper .widget {
        margin-bottom: 50px;
        
    }
    .side-bar .content-wrapper h4 {
        font-size: 18px;
        font-weight: 400;
        letter-spacing: 1px;
        line-height: 18px;
        margin-bottom: 28px;
        color: rgb(9, 41, 51)
    }
    .side-bar .content-wrapper p {
        color: rgb(166, 175, 179);
        font-size: 22px;
        font-weight: 400;
        line-height: 30.8px;
    }
    .side-bar .content-wrapper ul {
        list-style: none;
        padding: 0;     
    }
    .side-bar .content-wrapper ul li {
        color: rgb(97, 106, 125);
        align-items: start;
        display: flex;
    }
    .side-bar .content-wrapper ul li > div {
        display: inline-block;
    }
    .side-bar .content-wrapper ul li > div p {
        margin: -4px 0 0 12px;
    }
    
    .navbar-nav .nav-item .nav-link:hover {
        color: var(--main-color);
    }
    
    @include md {
        .navbar-nav {
            background-color: #fff !important;
            padding: 20px 0;
        }
        .navbar-nav .nav-item .nav-link {
            background-color: #fff !important;
            color: #000;
        }
    }
</style>