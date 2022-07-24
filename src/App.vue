<template>
  <div>
    <TheHeader />
    <MainContent />
    <TheFooter />
  </div>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";
import MainContent from "./components/MainContent.vue";
import TheFooter from "./components/TheFooter.vue";

export default {
  name: "App",
  components: { TheHeader, MainContent, TheFooter },
};
</script>

<style lang="scss">
@import "./assets/sass/style.scss";
</style>
