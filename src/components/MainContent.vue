<template>
  <main id="main-content">
    <section id="main-banner"></section>
    <section id="main-content">
      <div class="container">
        <div class="main-content__title">Current Series</div>
        <div class="main-content__comics-wrapper">
          <ComicCard
            v-for="(comic, i) in comics"
            :key="i"
            :img="comic.thumb"
            :name="comic.series"
          />
        </div>
        <button class="main-content__load-more">Load more</button>
      </div>
    </section>
    <ContentNav />
  </main>
</template>


<script>
import ContentNav from "./ContentNav.vue";
import ComicCard from "./ComicCard.vue";

export default {
  name: "MainContent",
  components: {
    ComicCard,
    ContentNav,
  },
  data() {
    return {
      comics: [
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
        },
      ],
    };
  },
};
</script>

<style lang='scss' scoped>
@import "../assets/scss/mixins.scss";

main {
  color: white;

  #main-banner {
    background: url("../assets/img/jumbotron.jpg") no-repeat;
    background-size: cover;
    background-position: top;
    height: 400px;
  }

  #main-content {
    background-color: #1c1c1c;
    color: white;

    .container {
      @include container;
      @include banner;
      min-height: 150px;
      justify-content: center;
      position: relative;
      flex-direction: column;
      gap: 35px;
      padding: 50px 15px 20px;

      .main-content__title,
      .main-content__load-more {
        border: 0;
        background-color: #0282f9;
        text-transform: uppercase;
        font-weight: 600;
      }

      .main-content__title {
        font-size: 20px;
        padding: 15px 30px;
        position: absolute;
        top: 0;
        left: 0;
        transform: translateY(-50%);
      }

      .main-content__load-more {
        color: white;
        padding: 12px 60px;
        font-size: 15px;
      }

      .main-content__comics-wrapper {
        display: flex;
        flex-wrap: wrap;
        gap: 50px 2%;
      }
    }
  }
}
</style>