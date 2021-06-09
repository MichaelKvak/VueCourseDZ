<template>
  <div class="container">
    <label>
      <input type="text" placeholder="login" v-model="log" />
    </label>
    <label>
      <input type="number" placeholder="password" v-model="pas" />
    </label>

    <label>
      <span v-if="log == 'admin'">
        <img :src="imageSrc" alt="smile" width="100px" height="100px"
      /></span>
      <span v-else-if="log == ''"></span>
      <span v-else :class="getClass()">error</span>
      <button @click="goIt">go</button>
    </label>
  </div>
</template>

<script>
export default {
  name: "LogPass",
  data() {
    return {
      log: "",
      pas: "",
    };
  },
  props: {
    imageSrc: {
      type: String,
      default: "https://clipart-best.com/img/smiley/smiley-clip-art-135.png",
    },
  },
  methods: {
    getClass() {
      return this.log == "ivan" ? "in" : "out";
    },
    goIt() {
      if (this.log == "admin") {
        alert("You are logined");
      } else {
        alert("try againe");
      }
    },
  },
};
</script>

<style lang="css" scoped>
.container {
  display: flex;
  flex-direction: column;
}
.in {
  color: blue;
}
.out {
  color: crimson;
}
</style>
