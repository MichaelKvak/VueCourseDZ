<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
   
    <curs/>
    <prognostic/>
    <translate/>
    <logpas/>
  </div>
</template>

<script>

import curs from './components/curs';
import prognostic from './components/prognostic.vue';
import translate from './components/translate.vue'
import logpas from './components/logpas'
export default {
  name: 'App',
  components: {
       curs,
       prognostic,
       translate,
       logpas
        
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
