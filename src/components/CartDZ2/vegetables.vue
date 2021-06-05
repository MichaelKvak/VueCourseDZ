<template>
    <div>
        <table border="4">
            <thead>
                    <td>fruits</td>
                    <td>price</td>
            </thead>
            <tbody>
                <tr v-for="veg in vegList" :key="veg">
                    <td>{{veg.fruits}}</td>
                    <td>{{veg.price}}</td>
                </tr>
            </tbody>
        </table>

    </div>
</template>

<script>
    export default {
        name:"vegetables",
        props:{
            vegList:{
                 type: Array,
                 default: ()=>[]
            },
            price:{
                type: [Number, String],
                default: null
            }

        }
        
    }
</script>

<style lang="scss" scoped>

</style>