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
  }
}
</script>

<style lang="scss">
*{
  margin: 0 auto;
  padding: 0;
}
.container{
  max-width: 1400px;
}
img{
  max-width: 100%;
}
body{
  background-color: black;
}
</style>
