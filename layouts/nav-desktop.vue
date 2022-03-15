<template>
  <div>
    <v-app-bar class="navbar" absolute color="transparent" flat>
      <v-img :src="require('@/static/logo.svg')" contain class="logo" />
      <span class="menu-item" v-for="(item, index) in menu" :key="index">
        {{ item.name }}
      </span>
    </v-app-bar>
  </div>
</template>
<script>
export default {
  name: "NavDesktop",
  props: {
    menu: {
      type: Array,
      default: null,
    },
  },
};
</script>

<style scoped>
.navbar {
  padding: 2rem;
}

.logo {
  max-width: 70px !important;
  margin-right: 4rem;
  margin-bottom: 0.5rem;
}

.menu-item {
  font-size: clamp(0.8rem, 1.2vw, 1rem);
  margin: 0 1rem;
  font-weight: 600;
  cursor: pointer;
  position: relative;
  padding-bottom: 0.5rem ;
}

.menu-item:hover::after {
  display: block;
  content: "";
  position: absolute;
  bottom: 0;
  left: calc(50% - 15px);
  width: 30px;
  border-bottom: 2px solid white;
}
</style>
