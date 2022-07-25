<template>
  <section id="banner">
    <div class="container">
      <div class="row">
        <div v-for="item in bannerItems" :key="item" class="col">
          <img :src="item.src" :alt="item.text" />
          <span>{{ item.text }}</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "BannerSection",
  props: {
    bannerItems: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "./../assets/sass/style.scss";

// | Content Banner Section
#banner {
  background-color: $primary;
  color: white;

  .col {
    @include flex_center("cross");
    padding: 2rem;

    img {
      height: 40px;
      max-width: 40px;
    }
    span {
      text-transform: uppercase;
      font-size: 0.6rem;
      padding-left: 1rem;
    }
  }
}
</style>
