<template>
  <div>
    <span v-if="$i18n.locale === 'en'" @click="switchLang">العربية</span>
    <span v-if="$i18n.locale === 'ar'" @click="switchLang">English</span>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    async switchLang() {
      if (this.$i18n.locale === "en") {
        await this.$router.replace(this.switchLocalePath("ar"));
      } else {
        await this.$router.replace(this.switchLocalePath("en"));
      }
      this.$router.go();
    },
  },
};
</script>

<style scoped lang="scss">
span {
  font-weight: 600;
  margin: 0 10px;
  cursor: pointer;
  color: #fff;
}
</style>
