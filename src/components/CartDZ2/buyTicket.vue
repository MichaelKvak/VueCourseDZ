<template>
    <div class="container">
<div class="logo">
    <img :src="imageLogo" alt="logo" width="100" height="100">
</div>
<div>
    <img :src="imageMain" alt="mainImage">
</div>
<div class="btm">
    <button @click="result" class="btnn"> byu ticket </button>
</div>
<div class="moviName">
    <p>
        {{moviName}}
    </p>
</div>
    </div>
</template>

<script>
    export default {
        name: 'buyTicket',
        props: {
            imageLogo:{
                type: String,
                default: 'No image'
            },
            imageMain: {
                type: String,
                default: 'No image'
            },
            moviName: {
                type: String,
                default: 'today no movi'
            },
           
        },
        methods: {
            result() {
                alert('You byu your ticket, see you later')
            }

        }

    }
</script>

<style lang="css" scoped>

.container {
    display: flex;
    flex-direction: column;
    }
.logo {
     top: 50px;
     margin-left: 400px;
   
}
.btm {
    top: 340px;
    margin-right: 245px;
    
}
.moviName{
     top: 350px;
     margin-right: 230px;
     text-size-adjust: 50;

}
.btnn{
background: linear-gradient(150deg, rgb(5, 5, 5) 0%, rgb(245, 244, 245) 100%);
color: rgb(248, 248, 248);
}



</style>