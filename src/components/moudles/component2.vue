<template>
    <div class="">
          <!-- 子父组件传参 -->
        <div class="">  
            <span>向父组件发送数据：{{childValue}}</span>
            <el-button type="primary" @click="reverse()">发送父组件的信息</el-button>
        </div>
    </div>
</template>

<script>
export default {
    data() { 
        return {
            //子父组件传参
            childValue:"子组件的数据test"
        }
    },

    mounted(){},

    methods:{
        reverse(){
            this.$emit('childValue',this.childValue)
        }
    },
}
</script>

<style scoped>

</style>