<template>
  <v-app class="window">
    <v-main>
      <Nuxt />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "DefaultLayout",
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Spartan:wght@500;600;700&display=swap');

:root {
  --DarkGray: hsl(0, 0%, 63%);
  --Black: hsl(0, 0%, 0%);
  --White: hsl(0, 0%, 100%);
  --VeryDarkGray: hsl(0, 0%, 27%);
}

.window {
  font-family: "Spartan";
  background: var(--White) !important;
}
</style>
