<template>
	<view class="content">
		<view class="text-area">
			<!-- #ifdef H5 -->
			<text @click="show()" class="title">H5</text>
			<!-- #endif -->
			<!-- #ifdef APP-ANDROID -->
			<text @click="show()" class="title">安卓平台</text>
			<!-- #endif -->
			<!-- #ifdef MP-WEIXIN -->
			<text @click="show()" class="title">微信小程序</text>
			<!-- #endif -->
			<!-- #ifdef APP-IOS -->
			<text @click="show()" class="title">IOS平台</text>
			<!-- #endif -->
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods:
		{
			show()
			{
				// #ifdef H5
				uni.showModal({
					title:'提示',
					content:'当前编译的是H5代码',
					showCancel:false,
				})
				// #endif
				// #ifdef APP-ANDROID
				uni.showModal({
					title:'提示',
					content:'当前编译的是安卓代码',
					showCancel:false,
				})
				// #endif
				// #ifdef MP-WEIXIN
				uni.showModal({
					title:'提示',
					content:'当前编译的是微信小程序代码',
					showCancel:false,
				})
				// #endif
				// #ifdef APP-IOS
				uni.showModal({
					title:'提示',
					content:'当前编译的是IOS代码',
					showCancel:false,
				})
				// #endif
			}
		}
	}
</script>

<style>
	.content
	{
		/* #ifdef H5 */
		background-color: aquamarine;
		/* #endif */
		/* #ifdef APP-ANDROID */
		background-color: red;
		/* #endif */
		/* #ifdef MP-WEIXIN */
		background-color: greenyellow;
		/* #endif */
		/* #ifdef APP-IOS */
		background-color: blueviolet;
		/* #endif */
	}
</style>
