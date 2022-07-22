<template>
  <div>
    <TheHeader />
    <MainContent />
  </div>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";
import MainContent from "./components/MainContent.vue";

export default {
  name: "App",
  components: { TheHeader, MainContent },
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
