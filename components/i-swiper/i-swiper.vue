<template>
	<swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000">
		<swiper-item class="flex justify-center" v-for="(item,index) in data" :key="index">
			<view class="swiper-item rounded shadow" @click="handleToDetail(item)">
				<image :src="item.src">
				</image>
			</view>
		</swiper-item>
	</swiper>
</template>

<script>
	export default {
		name: "i-swiper",
		props:{
			data:{
				type:Array,
				default:()=>[]
			}
		},
		data() {
			return {
			};
		},
		methods:{
			handleToDetail(item){
				this.$emit("click",item)
			}
		}
	}
</script>

<style>
	swiper{
		height: 310rpx;
		padding: 0 10rpx;
	}
	.swiper-item{
		width: 100%;
		height: 300rpx;
		overflow: hidden;
	}
	.swiper-item image{
		width: 100%;
		height: 100%;
	}
</style>
