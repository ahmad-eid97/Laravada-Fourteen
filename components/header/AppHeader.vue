<template>
  <header
    :class="!topOfPage ? 'onScroll' : ''"
    class="header header-style-2 clearfix"
  >
    <div class="row m-0 w-100">
      <b-navbar toggleable="lg">
        <b-navbar-brand href="#">
          <img
            src="/assets/logo2.png"
            alt=""
            style="width: 200px; margin: 15px 0"
          />
        </b-navbar-brand>

        <div class="d-flex align-items-center">
          <div class="smallScr">
            <langSwitch />
          </div>

          <b-navbar-toggle target="navbar-toggle-collapse">
            <template #default="{ expanded }">
              <span
                class="menu-trigger"
                :class="expanded ? 'active' : ''"
                id="menu03"
              >
                <p></p>
                <p></p>
                <p></p>
              </span>
            </template>
          </b-navbar-toggle>
        </div>

        <b-collapse
          id="navbar-toggle-collapse"
          class="ml-auto justify-content-end"
          is-nav
        >
          <b-navbar-nav class="align-items-center">
            <b-nav-item
              active-class="active"
              :to="localePath(`/${item.link}`)"
              exact
              v-for="item in $store.state.topMenu"
              :key="item.id"
            >
              <span v-if="!item.child.length">{{ item.label }}</span>

              <b-dropdown
                :text="item.label"
                block
                class="m-2 dropdownBtn"
                v-if="item.child.length"
              >
                <b-dropdown-item
                  v-for="child in item.child"
                  :key="child.id"
                  :to="localePath('/' + child.link)"
                  >{{ child.label }}</b-dropdown-item
                >
              </b-dropdown>
            </b-nav-item>
            <b-nav-item
              v-if="$store.state.user"
              @click="logout"
              class="outLarge"
            >
              Logout
            </b-nav-item>
            <div class="largeScr">
              <langSwitch />
            </div>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
  </header>
</template>

<script>
import langSwitch from "../langSwitch/langSwitch.vue";

export default {
  name: "AppHeader",
  components: {
    langSwitch,
  },
  data() {
    return {
      topOfPage: true,
    };
  },
  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  },
  mounted() {},
  methods: {
    handleScroll() {
      if (window.pageYOffset > 30) {
        if (this.topOfPage) this.topOfPage = false;
      } else {
        if (!this.topOfPage) this.topOfPage = true;
      }
    },
  },
};
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
  transition: all 0.2s ease-in-out;
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
  & > .dropdown {
    display: none;
  }
}
.navbar .nav-item .nav-link {
  background-clip: border-box;
  background-color: rgba(0, 0, 0, 0);
  color: rgb(255, 255, 255);
  display: block;
  font-size: 16px;
  font-weight: 700;
  line-height: 20px;
  padding: 5px 0;
}
.onScroll .navbar .nav-item .nav-link {
  color: rgb(0, 0, 0);
}
.onScroll .nav-item.active::after,
.onScroll .nav-item:hover::after {
  background-color: rgb(0, 0, 0);
}

.nav-item.active::after,
.nav-item:hover::after {
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
  transition: all 0.3s cubic-bezier(0.42, 0.01, 0.58, 1);
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
  transition: all 0.4s ease;
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
  box-shadow: 0 0 5px 0 rgba(0, 0, 0, 0.15);
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
  color: rgb(9, 41, 51);
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

.largeScr {
  @include md {
    display: none;
  }
}

.smallScr {
  display: none;
  @include md {
    display: inline;
  }
}

.navbar-nav .nav-item .nav-link:hover {
  color: var(--main-color);
}
.outLarge {
  display: none;
  @include md {
    display: inline;
  }
}

@include md {
  .navbar-nav {
    background-color: #fff !important;
    padding: 10px 0;
  }
  .navbar-nav .nav-item .nav-link {
    background-color: #fff !important;
    color: #000;
  }
}
.dropdownBtn {
  margin: 0 !important;
  button {
    background: none !important;
    padding: 0 !important;
    text-transform: none !important;
    font-size: 1.1rem !important;
    font-family: unset !important;
    font-weight: 500 !important;
    box-shadow: none !important;
    border: none !important;
    min-width: unset !important;
    width: 100%;
    position: relative;
    top: -3px;
    @include md {
      color: #000 !important;
    }
  }
  .dropdown-menu {
    top: 40px !important;
  }
}
</style>
