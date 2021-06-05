<template>
    <div>
<table border="1" width=250px cellpadding="5" class="tab">
    <thead class="head">
          <td>number</td>
          <td>firstname</td>
    </thead>
        <tbody class="container">
            <tr v-for="pupil in pupilList" :key="pupil.id" >
                <td>{{pupil.number}}</td> 
                <td>{{pupil.firstname}}</td>
            </tr>
        </tbody>
</table>
    </div>
</template>

<script>
    export default {
        name:'pupils',
props: {
        pupilList:{
        type: Array,
        default: ()=>[]
    }
   },
    }
    
 
 
</script>

<style lang="css" scoped>
.tab{
    border: 2px solid black;
    color: rgb(42, 58, 18);
    text-align:center;
}
.head{
    background-color: rgb(44, 228, 212);
}
.container{
    background-color: rgb(169, 236, 245);
}

</style>