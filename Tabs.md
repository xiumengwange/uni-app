```javascript
<template>
	<view class="tabs">
		<view class="nav">
			<view>全部</view>
			<view class="active">推荐</view>
			<view>颜值</view>
			<view>英雄联盟</view>
			<view>王者荣耀</view>
			<view>QQ飞车</view>
			<view>绝地求生</view>
			<view>和平精英</view>
			<view>CF</view>
			<view>户外</view>
			<view>二次元</view>
		</view>
	</view>
</template>

<script>
	export default {
		name:"Tabs",
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss" scoped>	// scoped 作用域：只对当前页面有效
.tabs {
	height: 70rpx;
	line-height: 70rpx;
	font-size: 30rpx;
	background-color: #fe7235;
	color: #FFFFFF;
	
	.nav {
		display: flex;
		white-space: nowrap;
		overflow-x: auto;
		
		view {
			// opacity: 0.8;
			padding: 0 12rpx;
		}
		
		.active {
			font-size: 36rpx;
			font-weight: bold;
		}
	}
	
	.nav::-webkit-scrollbar {	// 去除H5端的滚动条
		display: none;
	}
}
</style>

```

