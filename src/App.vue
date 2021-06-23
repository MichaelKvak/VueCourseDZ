<template>
  <div>
    <!-- 3.Використовуємо компонент, як новий тег -->
    <social-book />
    <Buttton />
    <!-- <months /> -->

    <!-- <for-english-traine :word-list="wordList" /> -->
    <!-- <gameCart /> -->
  </div>
</template>
<script>
//1. Імпортуємо файл
import socialBook from "./components/DZ5/socialBook/socialBook.vue";
import buttton from "./components/DZ5/socialBook/buttton.vue";
// import months from "./components/DZ4/months.vue";
// import forEnglishTraine from "./components/DZ4/forEnglishTraine.vue";
// import gameCart from "./components/DZ5/game/gameCart.vue";
export default {
  name: "App",

  components: {
    //2.Реєстрація
    socialBook,
    buttton,
    // months,
    // forEnglishTraine,
    // gameCart,
  },
  data() {
    return {
      // wordList: [
      //   {
      //     id: 1,
      //     wordImage:
      //       "https://economtochka.com.ua/image/cache/b-103_1-700x850.jpg",
      //     engWord: "table",
      //     uaWord: "стіл",
      //   },
      //   {
      //     wordImage:
      //       "https://pavlyk.in.ua/wp-content/uploads/2016/07/ORI-Chair-2.jpg",
      //     engWord: "chair",
      //     uaWord: "стілець",
      //   },
      //   {
      //     wordImage: "https://ochakovo.ru/wp-content/uploads/2020/10/0-3.png",
      //     engWord: "beer",
      //     uaWord: "пиво",
      //   },
      // ],
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
