<template>
  <footer>
    <!-- Footer Top -->
    <FooterTop />
    <!-- Footer Bottom -->
    <FooterBottom />
  </footer>
</template>

<script>
import FooterTop from "./FooterTop.vue";
import FooterBottom from "./FooterBottom.vue";
export default {
  name: "TheFooter",
  components: { FooterTop, FooterBottom },
};
</script>

<style lang="scss" scoped>
@import "./../assets/sass/style.scss";
</style>
