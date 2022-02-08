<template>
  <div>
    <section class="container">
      <section id="links">
        <ul>
          <li class="list-item">DC COMICS</li>
          <li v-for="link in DcComics" :key="link.text">{{ link.text }}</li>
          <li class="list-item">SHOP</li>
          <li v-for="link in Shop" :key="link.text">
            {{ link.text }}
          </li>
        </ul>
        <ul>
          <li class="list-item">DC</li>
          <li v-for="link in Dc" :key="link.text">
            {{ link.text }}
          </li>
        </ul>
        <ul>
          <li class="list-item">SITES</li>
          <li v-for="link in Sites" :key="link.text">
            {{ link.text }}
          </li>
        </ul>
      </section>
      <section id="dc-img"></section>
    </section>
    <section id="socials">
      <button>SIGN-UP NOW!</button>
      <span>
        <p>FOLLOW US</p>
        <img src="../assets/footer-facebook.png" alt="" />
        <img src="../assets/footer-twitter.png" alt="" />
        <img src="../assets/footer-youtube.png" alt="" />
        <img src="../assets/footer-pinterest.png" alt="" />
        <img src="../assets/footer-periscope.png" alt="" />
      </span>
    </section>
  </div>
</template>

<script>
export default {
  name: "footer",
  data() {
    return {
      DcComics: [
        { text: "Characters" },
        { text: "Movies" },
        { text: "TV" },
        { text: "Games" },
        { text: "Videos" },
        { text: "News" },
      ],
      Dc: [
        { text: "Terms Of Use" },
        { text: "Privacy policy(New)" },
        { text: "Ad Choice" },
        { text: "Advertising" },
        { text: "Subscriptions" },
        { text: "Talent Workshops" },
        { text: "CPSC Certificates" },
        { text: "Ratings" },
        { text: "Shop Help" },
        { text: "Contact Us" },
      ],
      Sites: [
        { text: "DC" },
        { text: "MAD Magazine" },
        { text: "DC Kids" },
        { text: "DC Universe" },
        { text: "DC Power Visa" },
      ],
      Shop: [{ text: "Shop DC" }, { text: "Shop DC Collectibles" }],
    };
  },
};
</script>

<style scoped lang="scss">
div {
  background-image: url("../assets/footer-bg.jpg");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
}
.container {
  display: flex;
  flex-wrap: wrap;
}
#links {
  padding: 10px 0 10px 0;
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
  ul {
    width: calc(100% / 3);
  }
  h3 {
    color: white;
  }
}

.list-item {
  color: white;
  font-size: 20px;
  padding: 10px 0 10px 0;
}
li {
  list-style: none;
  color: gray;
  padding-right: 20px;
}
#dc-img {
  background-image: url("../assets/dc-logo-bg.png");
  background-position: center;
  display: flex;
  min-width: 562px;
}
#shop {
  padding: 10px 0 10px 0;
  display: inline;
}
#socials {
  padding: 30px 0 30px 0;
  display: flex;
  justify-content: space-between;
  background-color: #303030;
  flex-basis: 100%;
  height: 100px;
  button {
    background-color: #303030;
    border: 2px solid #0282f9;
    padding: 20px;
    color: white;
    text-align: center;
    line-height: 5px;
  }
}

span {
  display: flex;
  align-items: center;
  p {
    color: #0282f9;
    padding-right: 10px;
    font-size: 20px;
    font-weight: 800;
  }
  img {
    padding-right: 10px;
  }
}
</style>