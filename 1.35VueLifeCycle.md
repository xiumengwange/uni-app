```javascript
<template>
	<view>
		
	</view>
</template>

<script>
	export default {
		name:"VueLifeCycle",
		data() {
			return {
				
			};
		},
		beforeCreate() {
			// this指向创建实例，不能访问data\computed\prop\watch\methods
			// 此时页面没有动画数据，可以创建loading动画，等待页面加载完成隐藏
			console.log('挂载阶段1，实例初始化后')
		},
		created() {
			// 给每个属性添加getter和setter，代表把data中属性变成一个[响应式的数据]
			// 在此发生异步请求，挂载数据后，会自动触发页面更新
			console.log('挂载阶段1，在此遍历data返回对象所有的属性')
		},
		beforeMount() {
			// 还没挂载到页面上，此时可以再对数据进行最后一次修改
			console.log('挂载阶段1，模板与数据进行结合')
		},
		mounted() {
			// 可以在获取页面上真实dom节点，不管是什么框架，不要通过传统思想操作dom
			console.log('挂载阶段1，是的window.onload，组件（编译成虚拟对象）挂载到页上面')
		},
		beforeUpdate() {
			console.log('更新阶段2，响应式数据更新会调用，在检测数据变化')
		},
		updated() {
			console.log('更新阶段2，数据与视图结合，肉眼能够看到页面上的数据变化了，也可以在此获取最新的dom')
		},
		beforeDestroy() {
			console.log('销毁阶段3，可以移除定时器，解除事件，等等之类的操作')
		},
		destroyed() {
			// 包括此组件包含的所有子组件都被销毁，组件销毁之后会与其他页面的关系都会断开绑定
			console.log('销毁阶段3，实列销毁后会把当前组件实例上的所有的东西（data，envert）解绑定')
		}
	}
</script>

<style>

</style>

```

