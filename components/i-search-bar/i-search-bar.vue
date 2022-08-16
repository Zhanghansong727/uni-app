<template>
	<view class="search-bar">
		<uni-search-bar placeholder="请输入搜索内容" bgColor="#f5f5f1" @confirm="search" @input="input" ></uni-search-bar>
	</view>
</template>

<script>
	export default {
		data() {
			return {
			}
		}
	}
</script>

<style>
.search-bar{
	height: 120rpx;
	padding: 0;
}
</style>
