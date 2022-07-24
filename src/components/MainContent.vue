<template>
  <main>
    <!-- Coontent ToDo -->
    <section id="content-todo">
      <div class="container">
        <h2>--> Content goes here</h2>
      </div>
    </section>
    <!-- Others Sections TODO -->
  </main>
</template>

<script>
export default {
  name: "MainContent",
};
</script>

<style lang="scss" scoped>
@import "./../assets/sass/style.scss";

// # MainContent Component
#content-todo {
  background-color: $secondary;
  padding: 2rem 0;

  h2 {
    color: white;
  }
}
</style>
