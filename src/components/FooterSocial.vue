<template>
  <section id="footer-social">
    <div class="container">
      <button class="btn">Sign Up Now!</button>
      <nav class="social-bar">
        <h5><a href="#">Follow us</a></h5>
        <ul>
          <li v-for="(social, i) in socials" :key="i">
            <a :href="social.href"><img :src="social.img" alt="" /></a>
          </li>
        </ul>
      </nav>
    </div>
  </section>
</template>

<script>
export default {
  name: "FooterSocial",
  data() {
    return {
      socials: [
        {
          img: "../assets/img/footer-facebook.png",
          href: "#",
        },
        {
          img: "../assets/img/footer-twitter.png",
          href: "#",
        },
        {
          img: "../assets/img/footer-youtube.png",
          href: "#",
        },
        {
          img: "../assets/img/footer-pinterest.png",
          href: "#",
        },
        {
          img: "../assets/img/footer-periscope.png",
          href: "#",
        },
      ],
    };
  },
};
</script>

<style lang='scss' scoped>
@import "../assets/scss/mixins.scss";

#footer-social {
  background-color: #303030;

  .container {
    @include container;
    @include banner;
    justify-content: space-between;
    gap: 20px;
    padding: 30px 15px;

    .btn {
      border: 1px solid #0282f9;
      background-color: transparent;
      color: white;
      text-transform: uppercase;
      font-size: 16px;
      padding: 15px;
      white-space: nowrap;
    }

    .social-bar {
      @include banner;
      gap: 25px;

      h5 {
        color: #0282f9;
        font-size: 16px;
        text-transform: uppercase;
        white-space: nowrap;
      }

      ul {
        display: contents;

        li {
          img {
            min-width: 35px;
          }
        }
      }
    }
  }
}
</style>