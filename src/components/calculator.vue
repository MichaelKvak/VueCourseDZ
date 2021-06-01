<template>
    <div>
  <label>
            Number 1
            <input type="number" v-model="num1">
        </label> <br>
        <label>
            Number 2
            <input type="number" v-model="num2">
        </label> <br>
        <button @click="getSum">
            Add
        </button> <br>
        <label>
            Summ
            <input type="number" :value="resSum">
        </label>     
    </div>
</template>

<script>
    export default {
        name: 'calculator',
              data() {
            return {
                num1: 0,
                num2: 0,
                resSum:0
            }
         },
             methods: {
            getSum() {
              this.resSum=parseFloat(this.num1)+
              parseFloat(this.num2)  
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>