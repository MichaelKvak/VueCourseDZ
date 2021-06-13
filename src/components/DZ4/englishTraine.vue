<template>
  <div :class="borderColor" class="border">
    <span>
      {{ result }}
    </span>
    <div>
      <img :src="wordImage" alt="image" class="img" />
    </div>
    <div>
      <span>{{ wordTitle }} </span>
    </div>

    <div>
      <input type="text" placeholder="enter translation" v-model="ua" />
      <button @click="perevod">
        translate
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "englishTraine",
  data() {
    return {
      ua: "",
      element: "стіл",
      result: null,
      borderColor: null,
    };
  },
  props: {
    wordImage: {
      type: String,
      default: "",
    },
    wordTitle: {
      type: String,
      default: "",
    },
    cartList: {
      type: Array,
      default: () => [],
    },
  },
  methods: {
    perevod() {
      this.result = this.element == this.ua ? "good" : "no, try againe";
      this.borderColor = this.ua === this.element ? "yes" : "no";
    },
  },
};
</script>

<style lang="css" scoped>
.img {
  width: 150px;
  height: 150px;
}
.border {
  border-width: 1;
  border-color: rgb(8, 8, 8);
  border-style: solid;
  padding: 10px;
  width: 180px;
}

.yes {
  border-color: green;
  border-style: solid;
  padding: 10px;
  width: 180px;
  border-width: 1;
}

.no {
  border-color: red;
  border-width: 1;
  border-style: solid;
  padding: 10px;
  width: 180px;
}
</style>
