<template>
    <div>
        <label>
        uakraine word
<input type="text" v-model='ua'>
</label>
<label>
    english word
    <input type="text" v-model="transl"/>    Тут достатньо одностороньої прив"язки даних <input type="text" :value="transl"/>
      <button @click = "perevod">
                        translate
                    </button>
</label>
    </div>
</template>

<script>
    export default {
        name:'translate',
        data(){
            return{
             dictionary:{'кіт':'cat',
                         'пес':'dog',
                         'корова':'cow'},
            transl:'',
            ua:''
            

        }
    },
    methods:{
        perevod(){
         
           this.transl=this.dictionary[this.ua]

        }
    }
    }
    
</script>

<style lang="scss" scoped>

</style>
