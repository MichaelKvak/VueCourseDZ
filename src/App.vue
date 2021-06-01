<template>
  <div id="app">
<!--        
   <CartDZ2
image-src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQGFf77XwVTKdTny5MsNc2mOHI5hApQ6eL9pQ&usqp=CAU"
value="27,5"/> -->
<CartDZ2 v-for="(item,index) in datalist" :key="index"
:image-src="item.imageSrc"
:value="item.value"
/>
  
  </div>
</template>

<script>

import CartDZ2 from './components/CartDZ2/index'

export default {
  name: 'App',
  components: {
      CartDZ2
        
  },
  data() {
    return{
      datalist: [
{
  id:1,
  imageSrc:"https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQGFf77XwVTKdTny5MsNc2mOHI5hApQ6eL9pQ&usqp=CAU",
  value:"27,5"
},
{
  id:2,
  imageSrc:"https://img1.freepng.ru/20171220/joe/euro-icon-png-5a3a2409dbaae4.91687898151375975389984204.jpg",
  value:"34" 
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
