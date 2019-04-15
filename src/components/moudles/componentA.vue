<template>
    <div class="">
        <p>A组件传</p>
        <span>{{elementValue}}</span>
        <el-button  type="primary"
                    @click="elementByValue">主要按钮</el-button>
    </div>
</template>

<script>
import BUS from "../../middleware/bus.js"
export default {
    data() { 
        return {
            elementValue:"123456A组件数据456789"
        }
    },

    mounted(){},

    methods:{
        elementByValue(){
            console.log("45645")
            BUS.$emit("elementByValue",this.elementValue);
        }
    },
}
</script>

<style scoped>
</style>