<template>
<div>
  <header>
    <Header/>
  </header>
  <main>
    <Main/>
  </main>
  <footer>
    <Footer/>
  </footer>
</div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';
export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
  },
 
  
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.container{
  max-width: 1400px;
  margin: 0 auto;
}
img{
  max-width: 100%;
}
body{
  font-family: 'Lato', sans-serif;
  @import url('https://fonts.googleapis.com/css2?family=Lato:wght@100;300&family=Montserrat:wght@100&family=Open+Sans:wght@400;600;800&family=Roboto:wght@300&family=Rubik+Mono+One&display=swap');
  background-color: black;

}
</style>
