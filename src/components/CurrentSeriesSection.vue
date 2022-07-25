<template>
  <section id="current-series">
    <div class="container">
      <h4>Current Series</h4>
      <div class="row">
        <div v-for="cover in currentSeries" :key="cover.series" class="col card">
          <figure>
            <img :src="cover.thumb" :alt="cover.series" />
            <figcaption>{{ cover.series }}</figcaption>
          </figure>
        </div>
      </div>
      <!-- Load More Button -->
      <button class="btn">Load More</button>
    </div>
  </section>
</template>

<script>
export default {
  name: "CurrentSeries",
  props: {
    currentSeries: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "./../assets/sass/style.scss";

// | Current Series
#current-series {
  background-color: $secondary;
  padding: 2rem 0;
  position: relative;

  h4 {
    position: absolute;
    top: 0;
    transform: translateY(-50%);

    text-transform: uppercase;
    color: white;
    background-color: $primary;
    padding: 0.5rem 1.2rem;
  }
  .row {
    flex-wrap: wrap;
    margin: 0 -1rem;

    .col {
      width: calc(100% / 6 - 2rem);
      margin: 1rem;
    }

    .card {
      height: 180px;

      figure {
        height: 100%;
        width: 100%;

        img {
          height: 80%;
          width: 100%;
          object-fit: cover;
          object-position: top;
        }
        figcaption {
          color: white;
          font-size: 0.8rem;
          text-transform: uppercase;
        }
      }
    }
  }
  .btn {
    display: block;
    font-weight: bold;
    text-transform: uppercase;
    color: white;
    background-color: $primary;
    border: 2px solid $primary;
    padding: 0.5rem 3.5rem;
    margin: 4rem auto 0;
    cursor: pointer;
  }
}
</style>
