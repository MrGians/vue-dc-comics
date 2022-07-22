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
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
              </ul>
            </div>
            <!-- Shop List -->
            <div id="shop">
              <h4>Shop</h4>
              <ul>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
              </ul>
            </div>
          </div>
          <div class="col">
            <!-- DC -->
            <div id="dc">
              <h4>DC</h4>

              <ul>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
              </ul>
            </div>
          </div>
          <div class="col">
            <!-- Sites -->
            <div id="sites">
              <h4>Sites</h4>

              <ul>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
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
