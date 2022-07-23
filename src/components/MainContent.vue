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
// variables
$primary: #0282f9;
$secondary: #1c1c1c;
$tertiary: #303030;

/* Utils */
.container {
  max-width: 1000px;
  margin: 0 auto;
}

/* Component */
#content-todo {
  background-color: $secondary;
  padding: 2rem 0;

  h2 {
    color: white;
  }
}
</style>
