<template>
  <div>
    <div id="main-footer-container">
      <section class="container" id="figures">
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
  name: "MainFooter",
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
    };
  },
};
</script>

<style scoped lang="scss" >
#main-footer-container {
  background-color: #0282f9;
}
#figures {
  display: flex;
  justify-content: space-between;
  align-items: center;
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