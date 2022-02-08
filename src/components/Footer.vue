<template>
  <div>
      <section>
          <ul>
              <li><h3>DC COMICS</h3>
              <ul>
                  <li v-for="link in DcComics" :key="link.text">{{link.text}}</li>
              </ul>
              </li>
          </ul>
          <ul>
              <li><h3>DC</h3>
              <ul>
                  <li v-for="link in Dc" :key="link.text">
                      {{link.text}}
                  </li>
              </ul>
              </li>
          </ul>
          <ul>
              <li><h3>SITES</h3>
              <ul>
                  <li v-for="link in Sites" :key="link.text">
                      {{link.text}}
                  </li>
              </ul></li>
          </ul>
          <ul>
              <li><h3>SHOP</h3>
              <ul>
                  <li v-for="link in Shop" :key="link.text">
                      {{link.text}}
                  </li>
              </ul></li>
          </ul>
      </section>
      <section id="dc-img">
          <img src="../assets/dc-logo-bg.png" alt="">
      </section>
  </div>
</template>

<script>
export default {
name: 'footer',
data(){
    return{
        DcComics: [
            {text:'Characters'},
            {text:'Movies'},
            {text:'TV'},
            {text:'Games'},
            {text:'Videos'},
            {text:'News'},
            
        ],
        Dc: [
            {text:'Terms Of Use'},
            {text:'Privacy policy(New)'},
            {text:'Ad Choice'},
            {text:'Advertising'},
            {text:'Subscriptions'},
            {text:'Talent Workshops'},
            {text:'CPSC Certificates'},
            {text:'Ratings'},
            {text:'Shop Help'},
            {text:'Contact Us'},            
        ],
        Sites: [
            {text:'DC'},
            {text:'MAD Magazine'},
            {text:'DC Kids'},
            {text:'DC Universe'},
            {text:'DC Power Visa'},
        ],
        Shop: [
            {text:'Shop DC'},
            {text:'Shop DC Collectibles'},
        ],
        
    }
}
}
</script>

<style scoped>
div{
    background-image: url('../assets/footer-bg.jpg');
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    display: flex;
    justify-content: start;
    text-align: left;
}
section{
    flex-wrap: wrap;
}
h3{
    color: white;
}
 li{
     list-style: none;
     color: gray;
 }
 #dc-img{
 }
</style>