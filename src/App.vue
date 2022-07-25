<template>
  <div>
    <TheHeader :links="headerLinks" />
    <MainContent :current-series="currentSeries" :banner-items="bannerItems" />
    <TheFooter />
  </div>
</template>

<script>
// Data
import { currentSeries, bannerItems, headerLinks } from "./assets/data/index.js";
// Components
import TheHeader from "./components/TheHeader.vue";
import MainContent from "./components/MainContent.vue";
import TheFooter from "./components/TheFooter.vue";

export default {
  name: "App",
  components: { TheHeader, MainContent, TheFooter },
  data() {
    return {
      currentSeries,
      bannerItems,
      headerLinks,
    };
  },
};
</script>

<style lang="scss">
@import "./assets/sass/style.scss";
</style>
