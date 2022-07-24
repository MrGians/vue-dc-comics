<template>
  <section id="footer-bottom">
    <div class="container">
      <div class="row">
        <!-- SignUp Now Btn -->
        <div class="col">
          <a class="btn" href="#">Sign-up Now!</a>
        </div>
        <!-- Social Follow Links -->
        <div class="col social-links">
          <h4>Follow Us</h4>
          <a v-for="social in socialLinks" :key="social" href="#"
            ><img :src="social.src" :alt="social.text"
          /></a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "FooterBottom",
  data() {
    return {
      socialLinks: [
        { text: "Facebook", src: require("../assets/img/footer-facebook.png") },
        { text: "Periscope", src: require("../assets/img/footer-periscope.png") },
        { text: "Pinterest", src: require("../assets/img/footer-pinterest.png") },
        { text: "Twitter", src: require("../assets/img/footer-twitter.png") },
        { text: "Youtube", src: require("../assets/img/footer-youtube.png") },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "./../assets/sass/style.scss";

// # TheFooter Component | Footer Bottom
#footer-bottom {
  background-color: $tertiary;

  .row {
    @include flex_center("cross");

    justify-content: space-between;

    .col .btn {
      display: inline-block;
      text-transform: uppercase;
      color: white;
      padding: 0.5rem 0.8rem;
      border: 2px solid $primary;
      margin: 1.5rem 0;
    }

    .col.social-links {
      display: flex;

      & > * {
        padding: 0.5rem;
      }
      h4 {
        text-transform: uppercase;
        color: $primary;
      }
      a {
        display: inline-block;
        width: 40px;
        height: 40px;
        border-radius: 50%;

        img {
          width: 100%;
          height: 100%;
        }
      }
    }
  }
}
</style>
