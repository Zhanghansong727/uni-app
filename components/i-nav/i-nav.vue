<template>
	<view class="flex flex-wrap nav py-2">
		<view class="nav-item py-1 flex  flex-column justify-center align-center" v-for="(item,index) in data" :key="index">
			<image :src="item.src" mode="widthFix" hover-class="bg-light"></image>
			<text class="text-muted mt-1 font-sm">{{item.name}}</text>
		</view>
	</view>
</template>

<script>
	export default {
		name: "i-nav",
		props: {
			data: {
				type: Array,
				default: () => []
			}
		},
		data() {
			return {

			};
		}
	}
</script>

<style>
.nav-item{
	width: 25%;
}
.nav-item image{
	width: 70rpx;
	height:70rpx;
}
</style>
