<template>
    <div class="container">
        <table border="1" width="20px">
            <tr>
                <th>Назва валюти</th>
                <th>Курс у гривнях</th>
            </tr>
  <tr>
    <td ><img :src="imageSrc" alt="currency" ></td> 
    <td>{{value}}</td>
  </tr>
        </table>

    </div>
</template>

<script>
    export default {
        name:'CartDZ2',

        props:{
            imageSrc:{
                type: String,
                default: 'https://www.078.com.ua/upload/blog/fbe5d3fd9fca1b3accb2711209711bdc.jpg'
            },

            value:{
                type: Number,
                default: null
            }
        }
        
    }
</script>

<style lang="css" scoped>
.container {
   color: green;
   
   
}

</style>