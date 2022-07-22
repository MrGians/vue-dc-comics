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

<style>
/* Utils */
.container {
  max-width: 1000px;
  margin: 0 auto;
}

/* Component */
#content-todo {
  background-color: black;
  padding: 2rem 0;
}

h2 {
  color: white;
}
</style>
