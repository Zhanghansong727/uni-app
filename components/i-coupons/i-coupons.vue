<template>
	<view class="p-2">
		<scroll-view class="scroll-view " scroll-x="true">
			<view class="coupon" v-for="(item,index) in data" :key="item.id">
				<view>
					<text>￥{{item.price}}</text>
					<text class="coupon-text">适用课程：{{item.value.title}}</text>
				</view>
				<view>领取</view>
			</view>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		name:"i-coupons",
		props:{
			data:{
				type:Array,
				default:()=>[]
			}
		},
		data() {
			return {
				
			};
		}
	}
</script>

<style>
.scroll-view{
	width: 100%;
	white-space: nowrap;
}
.coupon{
	display: inline-flex;
	min-width: 310rpx;
	color: #fff;
	margin-right: 30rpx;
}
.coupon > view:first-child{
	padding: 20rpx 30rpx;
	background-color: #d39e00;
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	border-right: 4rpx dashed #fff;
}
.coupon > view:last-child{
	width: 120rpx;
	display: flex;
	align-items: center;
	justify-content: center;
	background-color: #ffc107;
	font-size: 30rpx!important
}
.coupon-text{
	font-size: 20rpx;
}
</style>