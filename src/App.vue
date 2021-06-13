<template>
  <div>
    <!-- 3.Використовуємо компонент, як новий тег -->
    <english-traine
      v-for="item in cartList"
      :key="item.id"
      :word-image="item.wordImage"
      :word-title="item.wordTitle"
    />
  </div>
</template>
<script>
//1. Імпортуємо файл
import englishTraine from "./components/DZ4/englishTraine.vue";
export default {
  name: "App",
  components: {
    //2.Реєстрація
    englishTraine,
  },
  data() {
    return {
      cartList: [
        {
          id: 1,
          wordImage:
            "https://economtochka.com.ua/image/cache/b-103_1-700x850.jpg",
          wordTitle: "table",
        },
      ],
    };
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
