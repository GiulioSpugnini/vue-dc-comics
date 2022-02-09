<template>
  <div>
    <div id="content">
      <main>
        <span id="current">CURRENT SERIES</span>
        <section id="jumbo"></section>
        <section class="container">
          <section>
            <ul id="cards">
              <li class="card-game" v-for="(game, index) in games" :key="index">
                <img :src="game.thumb" alt="" />
                <p>{{ game.series.toUpperCase() }}</p>
              </li>
            </ul>
            <span id="load-button"
              ><button><strong>LOAD MORE</strong></button></span
            >
          </section>
        </section>
      </main>
    </div>
    <div class="container">
      <section id="figures">
        <figure v-for="card in cards" :key="card.text">
          <img :src="card.imgUrl" alt="" />
          {{ card.text }}
        </figure>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: "Main",

  data() {
    return {
      cards: [
        {
          imgUrl: require("../assets/buy-comics-digital-comics.png"),
          text: "DIGITAL COMICS",
        },
        {
          imgUrl: require("../assets/buy-comics-merchandise.png"),
          text: "DC MERCHANDISE",
        },
        {
          imgUrl: require("../assets/buy-comics-shop-locator.png"),
          text: "SUBSCRIPTION",
        },
        {
          imgUrl: require("../assets/buy-comics-subscriptions.png"),
          text: "COMIC SHOP LOCATOR",
        },
        {
          imgUrl: require("../assets/buy-dc-power-visa.svg"),
          text: "DC POWER VISA",
        },
      ],
      games: [
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

<style scoped lang="scss">
#content {
  background-color: #1c1c1c;
  padding: 0px 0 50px 0;
  h2 {
    color: white;
  }
}
#jumbo {
  min-height: 400px;
  background-image: url(../assets/jumbotron.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: top;
}
#cards {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  .card-game {
    width: calc(100% / 6);
    list-style: none;
    color: white;
    margin-top: 60px;
    p {
      padding-top: 10px;
      font-size: 15px;
      word-wrap: break-word;
    }
  }
}
main{
  position: relative;
}
#current {
  position: absolute;
  top: 35%;
  left: 12%;
  background-color: #0282f9;
  color: white;
  padding: 20px 10px 20px 10px;
  font-size: 25px;
  width: 250px;
  text-align: center;
  font-weight: 600;
}
.card-game img {
  width: 200px;
  height: 200px;
  object-fit: cover;
  object-position: -100% 0;
}
#load-button {
  padding-top: 20px;
  display: flex;
  justify-content: center;
  button {
    background-color: #0282f9;
    color: white;
    padding: 10px 5px 10px 5px;
    border: 0;
    width: 200px;
  }
}

#figures {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
div {
  background-color: #0282f9;
}
figure {
  margin: 0;
  display: flex;
  align-items: center;
  align-items: center;
  color: white;
  padding: 30px 0 30px 0;

  img {
    max-width: 50px;
    padding-right: 10px;
  }
}
</style>