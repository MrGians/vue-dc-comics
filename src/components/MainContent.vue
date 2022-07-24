<template>
  <main>
    <!-- Coontent ToDo -->
    <section id="content-todo">
      <div class="container">
        <h2>--> Content goes here</h2>
      </div>
    </section>
    <!-- Bonus Section -->
    <section id="bonus">
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

// | Content To-Do
#content-todo {
  background-color: $secondary;
  padding: 2rem 0;

  h2 {
    color: white;
  }
}

// | Content Bonus
#bonus {
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
