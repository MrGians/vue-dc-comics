<template>
  <header>
    <div class="container">
      <!-- Main Navbar -->
      <nav id="navbar">
        <!-- DC Logo -->
        <img src="../assets/img/dc-logo.png" alt="DC Logo" />

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
  data() {
    return {
      currentLink: 1,
      links: [
        {
          text: "Characters",
          url: "#",
          current: false,
        },
        {
          text: "Comics",
          url: "#",
          current: true,
        },
        {
          text: "Movies",
          url: "#",
          current: false,
        },
        {
          text: "TV",
          url: "#",
          current: false,
        },
        {
          text: "Games",
          url: "#",
          current: false,
        },
        {
          text: "Collectibles",
          url: "#",
          current: false,
        },
        {
          text: "Videos",
          url: "#",
          current: false,
        },
        {
          text: "Fans",
          url: "#",
          current: false,
        },
        {
          text: "News",
          url: "#",
          current: false,
        },
        {
          text: "Shop",
          url: "#",
          current: false,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
/* Utils */
.container {
  max-width: 1000px;
  margin: 0 auto;
}

// variables
$primary: #0282f9;
$secondary: #1c1c1c;

/* Component Custom */
#navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 70px;

  img {
    display: block;
    width: 50px;
  }

  ul {
    list-style-type: none;
    display: flex;
    align-items: center;
    height: 100%;

    li {
      height: 100%;
      display: flex;
      align-items: center;

      a {
        display: inline-block;
        font-size: 0.6rem;
        font-weight: 700;
        text-decoration: none;
        text-transform: uppercase;
        color: $secondary;
        border-bottom: 2px solid transparent;
        padding: calc(35px + 2px - 0.6rem) 0.8rem;

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
