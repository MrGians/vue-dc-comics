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

<style>
/* generics */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Open Sans", sans-serif;
}
</style>
