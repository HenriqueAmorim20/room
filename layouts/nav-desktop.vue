<template>
  <div>
    Desktop
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
  padding: 1.5rem 0 0 2rem;
}
</style>
