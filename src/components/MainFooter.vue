<template>
  <footer>
    <section id="footer-nav">
      <div class="container">
        <nav>
          <div class="col" v-for="(col, i) in navLists" :key="i">
            <ul v-for="(list, y) in col" :key="y">
              <h4>{{ list.title }}</h4>
              <li v-for="(item, j) in list.items" :key="j">
                <a :href="item.href"> {{ item.text }} </a>
              </li>
            </ul>
          </div>
        </nav>
        <div class="bg-logo"></div>
      </div>
    </section>

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
  data() {
    return {
      navLists: [
        [
          {
            title: "DC Comics",
            items: [
              {
                text: "Characters",
                href: "#",
              },
              {
                text: "Comics",
                href: "#",
              },
              {
                text: "Movies",
                href: "#",
              },
              {
                text: "TV",
                href: "#",
              },
              {
                text: "Games",
                href: "#",
              },
              {
                text: "Collectibles",
                href: "#",
              },
              {
                text: "Videos",
                href: "#",
              },
              {
                text: "Fans",
                href: "#",
              },
              {
                text: "News",
                href: "#",
              },
              {
                text: "Shop",
                href: "#",
              },
            ],
          },
          {
            title: "Shop",
            items: [
              {
                text: "Shop DC",
                href: "#",
              },
              {
                text: "Shop DC Collectibles",
                href: "#",
              },
            ],
          },
        ],
        [
          {
            title: "DC",
            items: [
              {
                text: "Terms of Use",
                href: "#",
              },
              {
                text: "Privacy poolicy(New)",
                href: "#",
              },
              {
                text: "Ad Choices",
                href: "#",
              },
              {
                text: "Advertising",
                href: "#",
              },
              {
                text: "Jobs",
                href: "#",
              },
              {
                text: "Subscriptions",
                href: "#",
              },
              {
                text: "Talent Workshops",
                href: "#",
              },
              {
                text: "CPSC Certificates",
                href: "#",
              },
              {
                text: "Ratings",
                href: "#",
              },
              {
                text: "Shop Help",
                href: "#",
              },
              {
                text: "Contact Us",
                href: "#",
              },
            ],
          },
        ],
        [
          {
            title: "Sites",
            items: [
              {
                text: "DC",
                href: "#",
              },
              {
                text: "MAD Magazine",
                href: "#",
              },
              {
                text: "DC Kids",
                href: "#",
              },
              {
                text: "DC Universe",
                href: "#",
              },
              {
                text: "DC Power Visa",
                href: "#",
              },
            ],
          },
        ],
      ],
    };
  },
};
</script>

<style lang='scss' scoped>
@import "../assets/scss/mixins.scss";

.container {
  @include container;
  color: white;
}

#footer-nav {
  background: url("../assets/img/footer-bg.jpg") no-repeat center;
  background-size: cover;

  .container {
    overflow: hidden;
    display: flex;
    justify-content: space-between;
    padding: 0;
    position: relative;

    nav {
      min-width: 30%;
      padding: 45px 20px;
      display: flex;
      gap: 25px;

      .col {
        width: calc(100% / 3);

        ul{
            margin-bottom: 30px;

            h4 {
                font-size: 19px;
                font-weight: 600;
                margin-bottom: 14px;
                text-transform: uppercase;
            }

            li{
                font-size: 14px;
                color: #959595;
                line-height: 20px;
            }
        }
      }
    }

    .bg-logo {
      position: absolute;
      right: 0;
      top: -20px;
      bottom: -20px;
      width: 560px;   
      background: url("../assets/img/dc-logo-bg.png") no-repeat center;
      background-size: cover;
    }
  }
}
</style>