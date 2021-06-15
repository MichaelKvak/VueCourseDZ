<template>
  <div>
    <!-- 3.Використовуємо компонент, як новий тег -->
    <social-book />
  </div>
</template>
<script>
//1. Імпортуємо файл
import socialBook from "./components/DZ5/socialBook.vue";

export default {
  name: "App",

  components: {
    //2.Реєстрація
    socialBook,
  },
  data() {
    return {
      messages: [
        {
          id: 1,
          title: "test",
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
