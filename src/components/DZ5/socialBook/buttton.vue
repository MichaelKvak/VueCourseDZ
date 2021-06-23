<template>
  <div>
    likes {{ counter }}
    <button v-on:click="likes()" class="btmL">&#128077;</button>

    <button v-on:click="dislike()" class="btmDL">&#128078;</button>
  </div>
</template>

<script>
export default {
  name: "buttton",
  data() {
    return {
      counter: 0,
    };
  },
  methods: {
    dislike() {
      this.counter -= 1;
    },
    likes() {
      this.like = this.counter += 1;
    },
  },
};
</script>

<style lang="css" scoped>
.btmDL {
  background: linear-gradient(
    150deg,
    rgb(0, 183, 255) 0%,
    rgb(204, 242, 253) 100%
  );
}
.btmL {
  background: linear-gradient(
    150deg,
    rgb(0, 183, 255) 0%,
    rgb(204, 242, 253) 100%
  );
}
</style>
