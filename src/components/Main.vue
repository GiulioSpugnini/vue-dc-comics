<template>
  <div>
      <section>

      </section>
      <section>
          <figure v-for='card in cards' :key='card.text'>
              <img src="` ../assets/${card.imgUrl}`" alt="">
              {{card.text}}</figure>
      </section>
  </div>
</template>

<script>
export default {
name: 'Main',
data(){
    return{
        cards:[
            {imgUrl: 'buy-comics-digital-comics.png', text:'DIGITAL COMICS'},
            {imgUrl: 'buy-comics-merchandise.png', text:'DC MERCHANDISE'},
            {imgUrl: 'buy-comics-shop-locator.png', text:'SUBSCRIPTION'},
            {imgUrl: 'buy-comics-subscriptions.png', text:'COMIC SHOP LOCATOR'},
            {imgUrl: 'buy-comics-power-visa.svg', text:'DC POWER VISA'},
        ]
    }
}
}
</script>

<style scoped>
section{
    background-color: #0282f9;
}
 figure{
     color: white;
 }
</style>