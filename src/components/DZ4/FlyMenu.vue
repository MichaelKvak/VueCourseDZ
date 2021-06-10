<template>
  <div>
    <h1>BUY TICKET</h1>
    <form>
      <select v-model="selectedbox1">
        <option disablet value="" class="text">ticket class</option>
        <option value="Busines">Busines</option>
        <option value="Econom">Econom</option>
      </select>
      <select v-model="selectedbox2" v-if="selectedbox1 == 'Busines'">
        <option disablet value="" class="text">service</option>
        <option value="magazine">magazine</option>
        <option value="brandy">brandy</option>
      </select>
      <select v-model="selectedbox3" v-else>
        <option disablet value="" class="text">service</option>
        <option value="beer">beer</option>
        <option value="crisps">crisps</option>
      </select>

      <span>
        <br /><strong> your choose: </strong>
        <hr />
        <br />
        fly class: {{ selectedbox1 }} <br />
        <span v-if="selectedbox1 == 'Busines'">
          your busines preferences : {{ selectedbox2 }}
        </span>
        <br />
        <span v-if="selectedbox1 == 'Busines'">
          snack <input type="radio" name="snack" value="yes" />yes
          <input type="radio" name="snack" value="no" />no
        </span>
        <span v-else>
          your econom preferences :
          {{ selectedbox3 }}</span
        >
      </span>
    </form>
  </div>
</template>

<script>
export default {
  name: "FlyMenu",
  data() {
    return {
      selectedbox1: "",
      selectedbox2: "",
      selectedbox3: "",
      value: String,
    };
  },
};
</script>

<style lang="css" scoped>
.text {
  color: rgba(255, 0, 0, 0.4);
}
</style>
