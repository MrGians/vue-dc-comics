<template>
  <footer>
    <!-- Footer Top -->
    <section id="footer-top">
      <div class="container">
        <div class="row">
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
    </section>
    <!-- Footer Bottom -->
    <section id="footer-bottom"></section>
  </footer>
</template>

<script>
export default {
  name: "TheFooter",
  data() {
    return {
      dcComicsLinks: [
        {
          text: "Characters",
          url: "#",
        },
        {
          text: "Comics",
          url: "#",
        },
        {
          text: "Movies",
          url: "#",
        },
        {
          text: "TV",
          url: "#",
        },
        {
          text: "Games",
          url: "#",
        },
        {
          text: "Videos",
          url: "#",
        },
        {
          text: "News",
          url: "#",
        },
      ],
      shopLinks: [
        {
          text: "Shop DC",
          url: "#",
        },
        {
          text: "Shop DC Collectibles",
          url: "#",
        },
      ],
      dcLinks: [
        {
          text: "Terms Of Use",
          url: "#",
        },
        {
          text: "Privacy policy (New)",
          url: "#",
        },
        {
          text: "Ad Choices",
          url: "#",
        },
        {
          text: "Advertising",
          url: "#",
        },
        {
          text: "Jobs",
          url: "#",
        },
        {
          text: "Subscriptions",
          url: "#",
        },
        {
          text: "Talent Workshops",
          url: "#",
        },
        {
          text: "CPSC Certificates",
          url: "#",
        },
        {
          text: "Ratings",
          url: "#",
        },
        {
          text: "Shop Help",
          url: "#",
        },
        {
          text: "Contact Us",
          url: "#",
        },
      ],
      sitesLinks: [
        {
          text: "DC",
          url: "#",
        },
        {
          text: "MAD Magazine",
          url: "#",
        },
        {
          text: "DC Kids",
          url: "#",
        },
        {
          text: "DC Universe",
          url: "#",
        },
        {
          text: "DC Power Visa",
          url: "#",
        },
      ],
    };
  },
};
</script>

<style scoped>
/* Generics */
footer {
  background-color: grey; /* TODO CANCEL */
}

/* Utils */
.container {
  max-width: 1000px;
  margin: 0 auto;
}

/* Component */
#footer-top {
  background-image: url("../assets/img/footer-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  padding: 2rem;
}

#footer-top .row {
  display: flex;
}

#footer-top .col {
  padding-right: 2rem;
}
#footer-top h4 {
  color: white;
}
#footer-top ul {
  list-style-type: none;
  margin-bottom: 1rem;
}

ul li a {
  color: white;
  text-decoration: none;
  font-size: 0.65rem;
}
</style>
