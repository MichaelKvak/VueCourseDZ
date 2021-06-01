<template>
    <div>
    <label>
       <button @click = "enter">
           enter this buttom
       </button>
       <label>
           <input type="text" v-model='newprog'>
       </label>
     </label>
    </div>
</template>

<script>
    export default {
        name: 'prognostic',
        data () {
            return{
            prog: ['today will be all right',
                    'today will be bad day',
                    'today you will win'   
            ],
            newprog: ''
            
          
        }
    },
    methods: {
        enter() {
        this.newprog = this.prog[Math.floor(Math.random() * this.prog.length)];
        }
    }


    }
</script>

<style lang="scss" scoped>

</style>