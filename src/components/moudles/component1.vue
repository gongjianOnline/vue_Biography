<template>
    <div class="">
        <!-- 父子组件传参 -->
        <div class="distance">
            <span>接受父组件:{{inputName}}</span>
            <el-button type="primary" @click="Forward()">获取父组件的信息</el-button>
        </div>

        
    </div>
</template>

<script>
export default {
    // 父子组件传参
    props:['inputName'],
    data() { 
        return {
        }
    },

    mounted(){},

    methods:{
        Forward(){
            console.log(this.inputName);
            console.log(this.props)
        },
       
    },
}
</script>

<style scoped>
.distance{
    margin: 10px;
    padding: 10px;
    border: 1px #000 solid
}
</style>