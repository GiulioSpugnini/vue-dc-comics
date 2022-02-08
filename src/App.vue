<template>
<div>
  <header>
    <Header/>
  </header>
  <main>
    <Main/>
  </main>
</div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
export default {
  name: 'App',
  components: {
    Header,
    Main,
  }
}
</script>

<style lang="scss">
*{
  margin: 0 auto;
  padding: 0;
}
body{
  background-color: black;
}
</style>
