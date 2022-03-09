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
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

ul {
  list-style: none;
}

img {
  max-width: 100%;
}

a {
  color: currentColor;
  text-decoration: none;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>
