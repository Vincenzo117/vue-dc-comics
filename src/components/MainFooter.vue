<template>
  <footer class="footer">
    <!-- qui ci vanno le liste  -->

    <FooterSocial />
  </footer>
</template>

<script>
import FooterSocial from "./FooterSocial.vue";

export default {
  name: "MainFooter",
  components: {
    FooterSocial,
  },
};
</script>

<style lang='scss' scoped>
</style>