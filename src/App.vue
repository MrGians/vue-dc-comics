<template>
  <div>
    <TheHeader />
  </div>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";

export default {
  name: "App",
  components: { TheHeader },
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
