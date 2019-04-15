<template>
    <div class="">
        <p>B组件收</p>
        <span>{{name}}</span>
    </div>
</template>

<script>
import BUS from "../../middleware/bus.js"
export default {
    data() { 
        return {
            name:null,
        }
    },

    mounted(){
        BUS.$on('elementByValue',(data)=>{
            this.name = data
        })
    },

    methods:{},
 }
</script>

<style scoped>


</style>