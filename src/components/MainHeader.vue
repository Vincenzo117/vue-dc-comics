<template>
  <header>
    <div class="container">

      <figure class="logo">
        <img src="../assets/img/dc-logo.png" alt="" />
      </figure>

      <nav>
        <ul>
          <li
            v-for="(item, i) in navItems"
            :key="i"
            :class="item.active ? 'active' : ''"
          >
            <a :href="item.href">{{ item.text }}</a>
          </li>
        </ul>
      </nav>

    </div>
  </header>
</template>

<script>
export default {
  name: "MainHeader",
  data() {
    return {
      navItems: [
        {
          text: "Characters",
          href: "#",
          active: false,
        },
        {
          text: "Comics",
          href: "#",
          active: true,
        },
        {
          text: "Movies",
          href: "#",
          active: false,
        },
        {
          text: "TV",
          href: "#",
          active: false,
        },
        {
          text: "Games",
          href: "#",
          active: false,
        },
        {
          text: "Collectibles",
          href: "#",
          active: false,
        },
        {
          text: "Videos",
          href: "#",
          active: false,
        },
        {
          text: "Fans",
          href: "#",
          active: false,
        },
        {
          text: "News",
          href: "#",
          active: false,
        },
        {
          text: "Shop",
          href: "#",
          active: false,
        },
      ],
    };
  },
};
</script>

<style lang='scss' scoped>
@import "../assets/scss/mixins.scss";

.container {
  @include container;
  @include banner;
  justify-content: space-between;
  gap: 20px;

  .logo {
    width: 80px;
    min-width: 80px;
  }

  ul {
    display: flex;
    gap: 10px;

    li {
      text-transform: uppercase;
      font-weight: 600;
      font-size: 14px;
      position: relative;
      transition: color ease-in-out 100ms;

      &.active,
      &:hover {
        color: #0082f9;
      }

      &.active:after {
        content: " ";
        height: 4px;
        position: absolute;
        left: 0;
        right: 0;
        top: 62px;
        background-color: #0082f9;
      }
    }
  }
}
</style>