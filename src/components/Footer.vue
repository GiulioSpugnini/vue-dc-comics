<template>
  <div>
    <div class="container">
      <section id="links">
        <ul>
          <li class="list-item">
            <h3>DC COMICS</h3>
            <ul>
              <li v-for="link in DcComics" :key="link.text">{{ link.text }}</li>
            </ul>
          </li>
        </ul>
        <ul>
          <li class="list-item">
            <h3>DC</h3>
            <ul>
              <li v-for="link in Dc" :key="link.text">
                {{ link.text }}
              </li>
            </ul>
          </li>
        </ul>
        <ul>
          <li class="list-item">
            <h3>SITES</h3>
            <ul>
              <li v-for="link in Sites" :key="link.text">
                {{ link.text }}
              </li>
            </ul>
          </li>
        </ul>
        <ul>
          <li class="list-item">
            <h3>SHOP</h3>
            <ul>
              <li v-for="link in Shop" :key="link.text">
                {{ link.text }}
              </li>
            </ul>
          </li>
        </ul>
      </section>
      <section id="dc-img">
        <!-- <img src="../assets/dc-logo-bg.png" alt=""> -->
      </section>
    </div>
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
  display: flex;
  flex-wrap: wrap;
}
.container {
  max-width: 1400px;
}
#links {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  width: 50%;
}
#links ul {
  width: calc(100% / 3);
}
h3 {
  color: white;
}
.list-item{
    text-align: left;
}
li {
  list-style: none;
  color: gray;
  padding-right: 20px;
}
#dc-img {
  background-image: url("../assets/dc-logo-bg.png");
  display: flex;
  min-width: 562px;
}
#socials {
    padding: 10px 0 10px 0;
    display: flex;
    justify-content: space-between;
  background-color: #303030;
  flex-basis: 100%;
}
button {
    background-color: #303030;
    border: 2px solid #0282f9;
  padding: 5px 10px 5px 10px;
  color: white;
}
p {
  color: #0282f9;
}
</style>