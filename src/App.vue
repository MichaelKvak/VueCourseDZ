<template>
  <div id="app">
   <pupils :pupil-list="pupilList"/> 
  </div>
</template>

<script>


import pupils from './components/CartDZ2/pupils.vue'
export default {
  name: 'App',
  components: {
      pupils
  },
  data() {
    return{
     pupilList: [
{
    id:1,
    number: 1,
    firstname: "Іванов І.І"
},
{
  id:2,
  firstname: "Жирков Я.Я.",
  number: 2
},
{
  id:3,
  firstname: "Коновалов Р.Н.",
  number: 3
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
