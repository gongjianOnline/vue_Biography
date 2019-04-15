<!-- 
	*测试： vue-cli中的父子组件、兄弟组件、子父组件传参
-->
<template>
	<div class="">
		<!-- 父子组件传参 -->
		<Component1  :inputName="name"></Component1>
		<!-- 子父组件传参 -->
		<div class="distance">
			<p>父组件接收:{{childValueName}}</p>
			<Component2  @childValue="childValue"></Component2>
		</div>
		<!-- 兄弟组件传参 -->
		<div class="distance">
			<p>兄弟组件传参</p>
			<ComponentA></ComponentA>
			<ComponentB></ComponentB>
		</div>
	</div>
</template>

<script>
import Component1 from "./moudles/component1"
import Component2 from "./moudles/component2" 
import ComponentA from "./moudles/componentA" 
import ComponentB from "./moudles/componentB" 

export default {
	components:{
		Component1,
		Component2,
		ComponentA,
		ComponentB
	},
	data () {
		return {
			name:"父组件信息发送",
			childValueName:null
		}
	},
	methods:{
		childValue(data){
			this.childValueName = data
			console.log(data)
		}
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.distance{
    margin: 10px;
    padding: 10px;
    border: 1px #000 solid
}
</style>

