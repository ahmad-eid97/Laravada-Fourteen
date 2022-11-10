<template>
  <footer>
    <div class="copyrights">
      <p>© Rail Coder 2022-2023. All rights reserved.</p>
      <div class="inline">
        <span class="mx-2">
          <font-awesome-icon icon="fa-solid fa-envelope" />
          info@railcoder.com
        </span>
        <p class="mx-2">
          <font-awesome-icon icon="fa-solid fa-square-phone" />
          +1111111111111
        </p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
  components: {},
  data() {
    return {};
  },
  beforeMount() {},
  methods: {},
};
</script>
<style lang="scss">
footer .copyrights {
  padding: 20px 65px;
  background-color: #18191b;
  display: flex;
  justify-content: space-between;
  color: #fff !important;
}
.inline {
  display: inline;
}
@include xs {
  footer .copyrights {
    padding: 20px 15px;
    background-color: #18191b;
    display: block;
  }
}
footer .copyrights p {
  color: rgb(255, 255, 255);
  font-size: 13px;
  font-weight: 400;
  line-height: 18.2px;
  text-align: left;
  margin: 0;
}
</style>
