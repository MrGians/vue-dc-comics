<template>
  <section id="footer-top">
    <div class="container">
      <div class="row">
        <div class="col">
          <!-- Footer Top Links -->
          <div class="row links">
            <!-- Column | #1 -->
            <div class="col">
              <!-- DC Comics List -->
              <div id="dc-comics">
                <h4>DC Comics</h4>
                <ul>
                  <li v-for="(link, i) in dcComicsLinks" :key="i">
                    <a :href="link.url">{{ link.text }}</a>
                  </li>
                </ul>
              </div>
              <!-- Shop List -->
              <div id="shop">
                <h4>Shop</h4>
                <ul>
                  <li v-for="(link, i) in shopLinks" :key="i">
                    <a :href="link.url">{{ link.text }}</a>
                  </li>
                </ul>
              </div>
            </div>
            <div class="col">
              <!-- DC -->
              <div id="dc">
                <h4>DC</h4>
                <ul>
                  <li v-for="(link, i) in dcLinks" :key="i">
                    <a :href="link.url">{{ link.text }}</a>
                  </li>
                </ul>
              </div>
            </div>
            <div class="col">
              <!-- Sites -->
              <div id="sites">
                <h4>Sites</h4>
                <ul>
                  <li v-for="(link, i) in sitesLinks" :key="i">
                    <a :href="link.url">{{ link.text }}</a>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
        <div class="col logo">
          <!-- Footer Top Bg-logo -->
          <img src="../assets/img/dc-logo-bg.png" alt="DC Background Logo" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "FooterTop",
  props: {
    dcComicsLinks: Array,
    shopLinks: Array,
    dcLinks: Array,
    sitesLinks: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "./../assets/sass/style.scss";

// # TheFooter Component | Footer Top
#footer-top {
  background-image: url("../assets/img/footer-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;

  .row {
    justify-content: space-between;

    .col {
      padding-right: 2rem;

      .row.links {
        padding: 1.2rem;

        h4 {
          color: white;
          text-transform: uppercase;
        }

        ul {
          margin-bottom: 0.5rem;

          li {
            line-height: 0.8rem;

            a {
              font-size: 0.55rem;
              color: #adadad;
            }
          }
        }
      }
    }

    .col.logo {
      width: 450px;
      height: 250px;
      overflow: hidden;

      img {
        display: block;
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }
  }
}
</style>
