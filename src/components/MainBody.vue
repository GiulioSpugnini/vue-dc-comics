<template>
  <div>
    <section>
      <ul id="cards">
        <li class="card-game" v-for="(product, index) in products" :key="index">
          <img :src="product.thumb" alt="" />
          <p>{{ product.series.toUpperCase() }}</p>
        </li>
      </ul>
      <span id="load-button"
        ><button><strong>LOAD MORE</strong></button></span
      >
    </section>
  </div>
</template>

<script>
export default {
  name: "MainBody",
  props:[ "products"],
};
</script>

<style scoped lang="scss">
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
</style>