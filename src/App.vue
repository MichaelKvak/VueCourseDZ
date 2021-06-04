<template>
  <div id="app">
  <reclam-cart 
  image-src='http://komiwiki.syktsu.ru/images/thumb/e/ec/%D0%9E%D1%80%D0%B5%D0%BB.jpg/280px-%D0%9E%D1%80%D0%B5%D0%BB.jpg'
  images-logo='https://yt3.ggpht.com/ytc/AAUvwnjSe4fJZyLxyXr-kOYKJo6VGiSDgYsmvsIoiOnVHA=s88-c-k-c0x00ffffff-no-rj'
  reclam-title="Їж морковку, будеш бачити як орел"
  />

  </div>
</template>
<script>

import reclamCart from './components/CartDZ2/reclamCart.vue'
export default {
  name: 'App',
  components: {
  reclamCart    
  },
  data() {
    return {
reclamCartList: [
  {
  id:1,
  imageSrc: 'http://komiwiki.syktsu.ru/images/thumb/e/ec/%D0%9E%D1%80%D0%B5%D0%BB.jpg/280px-%D0%9E%D1%80%D0%B5%D0%BB.jpg',
 
  reclamTitle: "Їж морковку, будеш бачити як орел"
  },
 ]
   }
  },
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
