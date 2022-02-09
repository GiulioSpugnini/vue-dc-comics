<template>
  <div>
    <main>
      <div id="content">
        <span id="current">CURRENT SERIES</span>
        <MainHeader />
        <section class="container">
          <MainBody />
        </section>
      </div>
      <MainFooter />
    </main>
  </div>
</template>

<script>
import MainHeader from "./MainHeader.vue";
import MainBody from "./MainBody.vue";
import MainFooter from "./MainFooter.vue";
export default {
  name: "Main",
  components: {
    MainHeader,
    MainBody,
    MainFooter,
  },

  data() {
    return {};
  },
};
</script>

<style lang="scss">
#content {
  background-color: #1c1c1c;
  padding: 0px 0 50px 0;
  h2 {
    color: white;
  }
}
main {
  position: relative;
}
#current {
  position: absolute;
  top: 30%;
  left: 12%;
  background-color: #0282f9;
  color: white;
  padding: 20px 10px 20px 10px;
  font-size: 25px;
  width: 250px;
  text-align: center;
  font-weight: 600;
}
</style>