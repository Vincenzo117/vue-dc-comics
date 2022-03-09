<template>
  <div id="app">
    <MainHeader />
    <MainContent />
    <MainNav />
    <FooterNav />
    <MainFooter />
  </div>
</template>

<script>
import MainHeader from "./components/MainHeader.vue";
import MainContent from "./components/MainContent.vue";
import MainNav from "./components/MainNav.vue";
import FooterNav from "./components/FooterNav.vue";
import MainFooter from "./components/MainFooter.vue";

export default {
  name: "App",
  components: {
    MainHeader,
    MainContent,
    MainNav,
    FooterNav,
    MainFooter,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
