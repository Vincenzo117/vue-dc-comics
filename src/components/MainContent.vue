<template>
  <main id="main-content">
    <section id="main-content">
      <div class="container">
        <div>Content goes here</div>
      </div>
    </section>
    <ContentNav />
  </main>
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
@import "../assets/scss/mixins.scss";

main {
  color: white;

  #main-content {
    background-color: #1c1c1c;

    .container {
      @include container;
      @include banner;
      min-height: 150px;
      justify-content: center;
    }
  }

}
</style>