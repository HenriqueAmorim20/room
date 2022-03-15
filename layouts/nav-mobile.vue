<template>
  <div>
    <v-app-bar class="navbar" height="60" flat absolute color="transparent">
      <v-img
        :src="require('@/static/icon-hamburger.svg')"
        contain
        class="menu-icon"
        @click.stop="drawer = true"
      />
      <v-spacer></v-spacer>
      <v-img :src="require('@/static/logo.svg')" contain class="logo" />
      <v-spacer></v-spacer>
    </v-app-bar>
    <v-navigation-drawer v-model="drawer" fixed left class="drawer">
      <v-img
        class="icon-close"
        :src="require('@/static/icon-close.svg')"
        max-width="20px"
        aspect-ratio="1"
        @click.stop="drawer = !drawer"
      />
      <span class="menu-item" v-for="(item, index) in menu" :key="index">
        {{ item.name }}
      </span>
    </v-navigation-drawer>
  </div>
</template>
<script>
export default {
  name: "NavMobile",
  props: {
    menu: {
      type: Array,
      default: null,
    },
  },
  data() {
    return {
      drawer: false,
    };
  },
};
</script>
<style scoped>
.navbar {
  padding: 0rem 0.7rem;
}

.logo {
  max-width: 70px !important;
  margin-left: -35px;
}

.menu-icon {
  max-width: min(8vw, 30px) !important;
}

.drawer {
  width: 100% !important;
  height: max-content !important;
  background-color: #fff !important;
  padding: 7% 5%;
}

.drawer >>> * {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.icon-close {
  margin-right: 1.5rem;
}

.menu-item {
  font-weight: 600;
  font-size: clamp(0.7rem, 3.5vw, 1rem);
}
</style>
