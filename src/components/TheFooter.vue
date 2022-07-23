<template>
  <footer>
    <!-- Footer Top -->
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
    <!-- Footer Bottom -->
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

/* Component | Footer Top */
#footer-top {
  background-image: url("../assets/img/footer-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}

#footer-top .row {
  display: flex;
  justify-content: space-between;
}

#footer-top .col {
  padding-right: 2rem;
}

#footer-top .row.links {
  padding: 1.2rem;
}

#footer-top h4 {
  color: white;
  text-transform: uppercase;
}
#footer-top ul {
  list-style-type: none;
  margin-bottom: 0.5rem;
}

#footer-top ul li {
  line-height: 0.8rem;
}

#footer-top ul li a {
  font-size: 0.55rem;
  text-decoration: none;
  color: rgb(173, 173, 173);
}

#footer-top .col.logo {
  width: 450px;
  height: 250px;
  overflow: hidden;
}

#footer-top .col.logo img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
/* Component | Footer Bottom */
#footer-bottom {
  background-color: grey;
}

#footer-bottom .row {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

#footer-bottom .col .btn {
  text-decoration: none;
  text-transform: uppercase;
  display: inline-block;
  color: white;
  padding: 0.5rem 0.8rem;
  margin: 1.5rem 0;
  border: 2px solid blue;
}

#footer-bottom .social-links {
  display: flex;
}

#footer-bottom .social-links > * {
  padding: 0.5rem;
}

#footer-bottom .social-links h4 {
  text-transform: uppercase;
  color: blue;
}

#footer-bottom .social-links a {
  text-decoration: none;
  display: inline-block;
  width: 40px;
  height: 40px;
  border-radius: 50%;
}

#footer-bottom .social-links img {
  width: 100%;
  height: 100%;
}
</style>
