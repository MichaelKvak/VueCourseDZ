<template>
<div>
    <div class="container">
         <img :src="imageSrc" alt="reklama">
            <div class="text">
                <img :src="imageLogo" alt="logo" width="70px" height="60px">
                <p class="paragraph">
                {{reclamTitle}}
                Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                Provident unde officiis rem laboriosam eum ducimus autem 
                pariatur cumque earum similique facilis laborum, assumenda 
                numquam, ea quae consequatur natus quidem consectetur.
                </p>
            </div>
         
    </div>
  </div>
</template>

<script>
    export default {
        name: 'reclamCart',

        props: {
            imageSrc: {
                type: String,
                default: ""
            },

            imageLogo: {
                type: String,
                default: 'https://yt3.ggpht.com/ytc/AAUvwnjSe4fJZyLxyXr-kOYKJo6VGiSDgYsmvsIoiOnVHA=s88-c-k-c0x00ffffff-no-rj'
            },
            reclamTitle: {
                type: String,
                default: 'no title'
            }
        },
    }
</script>

<style lang="css" scoped>
.container{
    display: flex;
    flex-direction: row;
    justify-content: right;
    flex-basis: 200px; height: 300px
}
 .paragraph{
     width: 300px;
     height: 100%;
 }
 .text{
    text-align: right;
 }


</style>