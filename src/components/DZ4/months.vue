<template>
  <div>
    month1
    <input type="number" v-model.number="mon1" />
    month2
    <input type="number" v-model.number="mon2" />
    month3
    <input type="number" v-model.number="mon3" />
  </div>
</template>

<script>
export default {
  name: "months",
  data() {
    return {
      mon1: "",
      mon2: "",
      mon3: "",
    };
  },
  watch: {
    mon2: function(old) {
      this.mon3 = old + 1;
    },
    mon1: function(old) {
      this.mon2 = old + 1;
    },
    mon3: function(old) {
      this.mon1 = old - 2;
    },
  },
};
</script>

<style lang="css" scoped></style>
