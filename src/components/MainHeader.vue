<template>
  <header class="header">
    <figure class="logo">
      <img src="../assets/dc-logo.png" alt="" />
    </figure>
    <nav>
      <ul>
        <li v-for="(item, i) in navItems" :key="i" :class="item.active ? 'active' : ''">
            <a href="#">{{ item.text }}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "MainHeader",
  data() {
    return {
      navItems: [
        {
            text: 'Characters',
            active: true
        },
        {
            text: 'Comics',
            active: false
        },
        {
            text: 'Movies',
            active: false
        },
        {
            text: 'TV',
            active: false
        },
        {
            text: 'Games',
            active: false
        },
        {
            text: 'Collectibles',
            active: false
        },
        {
            text: 'Videos',
            active: false
        },
        {
            text: 'Fans',
            active: false
        },
        {
            text: 'News',
            active: false
        },
        {
            text: 'Shop',
            active: false
        }
      ],
    };
  },
};
</script>

<style lang='scss' scoped>
.header {
  padding: 15px 0;
  width: 80vw;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
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
      font-weight: 500;
      position: relative;

      &.active,
      &:hover {
        color: #0082f9;
      }

      &.active:after {
        content: " ";
        height: 5px;
        position: absolute;
        left: 0;
        right: 0;
        bottom: -0px;
        top: 60px;
        background-color: #0082f9;
      }
    }
  }
}
</style>