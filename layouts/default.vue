<template>
  <v-app class="window">
    <Navbar />
    <v-main>
      <Nuxt />
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
import Navbar from "./navbar.vue";
import Footer from "./footer.vue";

export default {
  name: "DefaultLayout",
  components: {
    Navbar,
    Footer,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Spartan:wght@500;600;700&display=swap");

:root {
  --DarkGray: hsl(0, 0%, 63%);
  --Black: hsl(0, 0%, 0%);
  --White: hsl(0, 0%, 100%);
  --VeryDarkGray: hsl(0, 0%, 27%);
}

.window {
  font-family: "Spartan";
  background: var(--White) !important;
  color: var(--Black) !important;
}
</style>
