<template>
    <div>
        <label>
            login
            <input type="text" v-model='log'>
        </label>
        <label>
            pass
            <input type="number" v-model='pas'>
        </label>
        <button @click="check">
            go
        </button>

    </div>
</template>

<script>
    export default {
        name:"logpas",
        data(){ 
            return{
            users:{"admin" : "123",
                   "mama" : "456",
                   "papa" : "789" }
            }
        
    },

    methods:{
           check(){
               if (this.pas == this.users[this.log]) {
    alert ("Привет!");
     
}
else {
    alert ("Неверный логин или пароль");
}
           }
    }
    }
    
</script>

<style lang="scss" scoped>

</style>