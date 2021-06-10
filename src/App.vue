<template>
  <div>
    <!-- 3.Використовуємо компонент, як новий тег -->
    <fly-menu />
  </div>
</template>
<script>
//1. Імпортуємо файл
import FlyMenu from "./components/DZ4/FlyMenu.vue";
export default {
  name: "App",
  components: {
    //2.Реєстрація
    FlyMenu,
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
