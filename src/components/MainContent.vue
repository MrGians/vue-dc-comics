<template>
  <main>
    <!-- Jumbotron -->
    <section id="jumbotron"></section>
    <!-- Current Series -->
    <section id="current-series">
      <div class="container">
        <h4>Current Series</h4>
      </div>
    </section>
    <!-- Banner Section -->
    <section id="banner">
      <div class="container">
        <div class="row">
          <div v-for="item in bonusItems" :key="item" class="col">
            <img :src="item.src" :alt="item.text" />
            <span>{{ item.text }}</span>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: "MainContent",
  props: {
    currentSeries: Array,
  },
  data() {
    return {
      bonusItems: [
        { text: "Digital Comics", src: require("../assets/img/buy-comics-digital-comics.png") },
        { text: "DC Merchandise", src: require("../assets/img/buy-comics-merchandise.png") },
        { text: "Subscription", src: require("../assets/img/buy-comics-subscriptions.png") },
        { text: "Comic Shop Locator", src: require("../assets/img/buy-comics-shop-locator.png") },
        { text: "DC Power Visa", src: require("../assets/img/buy-dc-power-visa.svg") },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "./../assets/sass/style.scss";

// # MainContent Component

// Jumbotron
#jumbotron {
  height: 300px;
  background-image: url("./../assets/img/jumbotron.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}
// | Current Series
#current-series {
  background-color: $secondary;
  padding: 2rem 0;

  h2 {
    color: white;
  }
}

// | Content Banner
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
