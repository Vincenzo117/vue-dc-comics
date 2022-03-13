<template>
  <div class="comic">
    <figure class="comic__thumb">
      <img :src="img" :alt="name" />
    </figure>
    <p class="comic__name">{{ name }}</p>
  </div>
</template>

<script>
export default {
  name: "ComicCard",
  props: {
    img: String,
    name: String,
  },
};
</script>

<style lang="scss" scoped>
.comic {
  width: calc(90% / 6);

  .comic__thumb {
    width: 100%;
    aspect-ratio: 1;
    overflow: hidden;
    margin-bottom: 20px;
  }

  .comic__name {
    font-size: 16px;
  }
}
</style>