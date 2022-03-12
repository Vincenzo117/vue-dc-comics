<template>
  <section id="content-nav">
    <div class="container">
      <ul>
        <li v-for="(item, i) in navItems" :key="i">
          <a :href="item.href">
            <img :src="item.img" alt="" />
            {{ item.text }}</a
          >
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: "ContentNav",
  data() {
    return {
      navItems: [
        {
          img: "../assets/img/buy-comics-digital-comics.png",
          text: "Digital Comics",
          href: "#",
        },
        {
          img: "../assets/img/buy-comics-merchandise.png",
          text: "DC Merchandise",
          href: "#",
        },
        {
          img: "../assets/img/buy-comics-subscriptions.png",
          text: "Subscription",
          href: "#",
        },
        {
          img: "../assets/img/buy-comics-shop-locator.png",
          text: "Comic Shop Locator",
          href: "#",
        },
        {
          img: "../assets/img/buy-comics-power-visa.png",
          text: "DC Power Visa",
          href: "#",
        },
      ],
    };
  },
};
</script>

<style lang='scss' scoped>
@import "../assets/scss/mixins.scss";

#content-nav {
  background-color: #0282f9;

  .container {
    @include container;
    @include banner;

    ul {
      flex-grow: 1;
      display: flex;
      gap: 15px;
      justify-content: space-around;

      li {
        width: max-content;

        a {
          @include banner;
          gap: 5px;
          text-transform: uppercase;
          white-space: nowrap;
          font-size: 14px;

          img {
            width: 45px;
          }
        }
      }
    }
  }
}
</style>