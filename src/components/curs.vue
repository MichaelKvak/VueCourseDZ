<template>
    <div>
        <label>
            grn
            <input type="number" v-model = "grn">
        </label>
            <label>
                doll
                <input type="number" :value = "doll">
            </label>
                <label>
                    <button @click = "perevod">
                        press
                    </button>
                </label>
    
    </div>
</template>

<script>
    export default {
        name: 'curs',
        data(){
            return{
                grn: 0,
                doll: 0,
                cursD: 27.5
                
            }
        },
        methods: {
            perevod() {
this.doll = parseFloat (this.grn) * this.cursD
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>