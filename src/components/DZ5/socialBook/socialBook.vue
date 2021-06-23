<template>
  <div>
    <span class="logo">
      <h1>Task Book</h1>
      <img
        src="https://www.nicepng.com/png/detail/208-2085876_message-comments-message-icon-black-png.png"
        alt="msg"
        width="30"
        height="30"
    /></span>
    <form @submit.prevent="addMessage">
      <input type="text" v-model="newMessageText" placeholder="write massage" />
      <button class="btm">sent message</button>
    </form>

    <ul>
      <li
        v-for="(message, i) in messages"
        :key="message.id"
        v-bind:index="i"
        v-bind:title="message.title"
        v-on:remove-message="removeMessage(i)"
      >
        {{ message.title }}

        <span>
          <buttton />
          <button class="btn" v-on:click="removeMessage(i)">
            &times;
          </button>
        </span>
      </li>
    </ul>
  </div>
</template>

<script>
import buttton from "./buttton.vue";
export default {
  components: { buttton },
  name: "socialBook",

  data() {
    return {
      counter: 0,
      message: 0,
      nextMessageId: 2,
      newMessageText: "",
    };
  },
  props: {
    messages: {
      type: Array,
      default: () => [],
    },
    index: Number,
  },
  methods: {
    removeMessage(i) {
      this.messages.splice(i, 1);
    },
    addMessage() {
      this.messages.push({
        id: this.nextMessageId++,
        title: this.newMessageText,
        counter: this.counter,
      });
      this.newMessageText = "";
      this.counter = 0;
    },
  },
};
</script>

<style lang="css" scoped>
li {
  list-style: none;
  margin: 0;
  padding: 0;
  border: 1px solid #ccc;
  display: flex;
  justify-content: space-between;
  padding: 0.5rem 2rem;
  margin-bottom: 1rem;
}
.btn {
  margin-left: 10px;
  background: linear-gradient(
    150deg,
    rgb(230, 114, 214) 0%,
    rgb(245, 244, 245) 100%
  );
  color: #fff;
  border-radius: 50%;
  font-weight: bold;
}
.btm {
  background: linear-gradient(
    150deg,
    rgb(0, 183, 255) 0%,
    rgb(204, 242, 253) 100%
  );
  color: rgb(255, 255, 255);
  border-radius: 50%;
  font-weight: bold;
}
.space {
  padding: 20px;
}
.done {
  text-decoration: line-through;
}
.NumArray {
  display: flex;
  margin-bottom: 20px;
  margin-left: 50px;
  font-weight: bold;
}
input {
  width: 250px;
  margin: 25px;
}
.logo {
  display: flex;
  flex-direction: row;
}
</style>
