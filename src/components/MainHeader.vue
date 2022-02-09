<template>
  <div>
    <section id="jumbo"></section>
  </div>
</template>

<script>
export default {
  name: "MainHeader",
};
</script>

<style scoped lang="scss">
#jumbo {
  min-height: 400px;
  background-image: url(../assets/jumbotron.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: top;
}
</style>