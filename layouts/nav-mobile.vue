<template>
  <div>
    Mobile
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
  padding: 0.7rem;
}
</style>
