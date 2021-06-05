<template>
  <div id="app">
 <buy-ticket v-for="(item,index) in moviList" :key="index"
            :image-logo="item.imageLogo"
            :image-main="item.imageMain"
            :movi-name="item.moviName"
         
 />
  </div>
</template>
<script>

import buyTicket from './components/CartDZ2/buyTicket.vue'
export default {
  name: 'App',
  components: {
   buyTicket
  },
  data() {
    return {
      moviList: [
        {
          id:1,
          imageLogo: 'https://cdn1.vectorstock.com/i/thumb-large/06/85/mountain-films-logo-design-inspiration-vector-24750685.jpg',
          imageMain: 'https://i.ytimg.com/vi/LR8x2sKK3Oc/mqdefault.jpg',
          moviName: 'Scarry Movi'
                  }
      ]

  }
 }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 50px;
}

</style>
