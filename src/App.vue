<template>
<div>
  <header>
    <Header/>
  </header>
</div>
</template>

<script>
import Header from './components/Header.vue';
export default {
  name: 'App',
  components: {
    Header,
  }
}
</script>

<style lang="scss">
*{
  margin: 0 auto;
  max-width: 1200px;
  padding: 0;
}
</style>
