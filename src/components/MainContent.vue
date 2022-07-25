<template>
  <main>
    <!-- Jumbotron -->
    <section id="jumbotron"></section>
    <!-- Current Series -->
    <CurrentSeriesSection :current-series="currentSeries" />
    <!-- Banner Section -->
    <BannerSection :banner-items="bannerItems" />
  </main>
</template>

<script>
// Components
import CurrentSeriesSection from "./CurrentSeriesSection.vue";
import BannerSection from "./BannerSection.vue";

export default {
  name: "MainContent",
  components: { CurrentSeriesSection, BannerSection },
  props: {
    currentSeries: Array,
    bannerItems: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "./../assets/sass/style.scss";

// Jumbotron
#jumbotron {
  height: 300px;
  background-image: url("./../assets/img/jumbotron.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
