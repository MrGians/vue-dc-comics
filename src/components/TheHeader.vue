<template>
  <header>
    <div class="container">
      <!-- Main Navbar -->
      <nav id="navbar">
        <!-- DC Logo -->
        <a href="#">
          <img src="../assets/img/dc-logo.png" alt="DC Logo" />
        </a>

        <!-- Navbar Links -->
        <ul>
          <li v-for="(link, i) in links" :key="i">
            <a :class="{ active: currentLink === i }" @click="currentLink = i" :href="link.url">
              {{ link.text }}
            </a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "TheHeader",
  props: {
    links: Array,
  },
  data() {
    return {
      currentLink: 1,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "./../assets/sass/style.scss";

// # TheHeader Component
#navbar {
  @include flex_center("cross");
  justify-content: space-between;
  height: 70px;

  img {
    display: block;
    width: 50px;
  }

  ul {
    @include flex_center("cross");
    height: 100%;

    li {
      height: 100%;
      @include flex_center("cross");

      a {
        display: inline-block;
        font-size: 0.6rem;
        font-weight: 700;
        color: $secondary;
        text-transform: uppercase;
        padding: calc(35px + 2px - 0.6rem) 0.8rem;
        border-bottom: 2px solid transparent;

        &:hover,
        &.active {
          color: $primary;
          border-bottom: 2px solid $primary;
        }
      }
    }
  }
}
</style>
