<template>
  <footer>
    <!-- Footer Top -->
    <FooterTop
      :dc-comics-links="dcComicsLinks"
      :shop-links="shopLinks"
      :dc-links="dcLinks"
      :sites-links="sitesLinks"
    />
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
  props: {
    dcComicsLinks: Array,
    shopLinks: Array,
    dcLinks: Array,
    sitesLinks: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "./../assets/sass/style.scss";
</style>
