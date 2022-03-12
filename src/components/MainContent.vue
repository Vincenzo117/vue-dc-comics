<template>
  <section id="main-content">
    <!-- qui il contenuto principale -->

    <ContentNav />
  </section>
</template>


<script>
import ContentNav from "./ContentNav.vue";
export default {
  name: "MainContent",
  components: {
    ContentNav,
  },
};
</script>

<style lang='scss' scoped>
</style>