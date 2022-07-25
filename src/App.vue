<template>
  <div>
    <TheHeader />
    <MainContent />
    <TheFooter />
  </div>
</template>

<script>
// Data
import currentSeries from "./assets/data/dc-comics.json";
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
    };
  },
};
</script>

<style lang="scss">
@import "./assets/sass/style.scss";
</style>
