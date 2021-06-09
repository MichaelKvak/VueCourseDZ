<template>
  <div>
    <!-- 3.Використовуємо компонент, як новий тег -->
    <log-pass />
  </div>
</template>
<script>
//1. Імпортуємо файл
import LogPass from "./components/DZ4/LogPass.vue";
export default {
  name: "App",
  components: {
    //2.Реєстрація
    LogPass,
  },
};
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
