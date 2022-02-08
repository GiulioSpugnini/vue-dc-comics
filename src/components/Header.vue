<template>
  <div>
      <figure>
          <img src="../assets/dc-logo.png" alt="">
      </figure>
      <nav>
          <ul>
              <li v-for='link in links' :key='link.text'>{{link.text}}</li>
          </ul>
      </nav>
  </div>
</template>

<script>
export default {
name: 'Header',
data(){
    return{
        links:[
            {text: 'CHARACTERS', url: '#', active:false},
            {text: 'COMICS', url: '#', active:false},
            {text: 'MOVIES', url: '#', active:false},
            {text: 'TV', url: '#', active:false},
            {text: 'GAMES', url: '#', active:false},
            {text: 'COLLECTIBLES', url: '#', active:false},
            {text: 'VIDEOS', url: '#', active:false},
            {text: 'FANS', url: '#', active:false},
            {text: 'NEWS', url: '#', active:false},
            {text: 'SHOP', url: '#', active:false},
        ],
};

},
};
</script>

<style scoped lang="scss">
    div{
     display: flex;
     justify-content: space-between;
     align-items: center;
     margin-top: 50px;
     padding-top: 20px;
     padding-bottom: 20px;
     background-color: #fff;
        ul{
        display: flex;
        justify-content: space-between;
            li{
             list-style: none;
             text-decoration: none;
             padding: 10px;
             font-weight: bolder;
            }
        }
    
    }
    
</style>