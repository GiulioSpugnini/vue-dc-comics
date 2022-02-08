<template>
  <div>
    <div id="content">
      <section class="container">
        <h2>Content goes here</h2>
      </section>
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
    };
  },
};
</script>

<style scoped lang="scss">
#content {
  background-color: black;
  padding: 50px 0 50px 0;
  h2 {
    color: white;
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