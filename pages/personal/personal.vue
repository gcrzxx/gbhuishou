<template>
	<view>
		<view class="personal-container">
			<view class="top-container">
				<image src="../../static/001.png"></image>
				<view class="name">用户ID</view>
			</view>
			<view class="order-container">
				<navigator class="nav-text" url="../order/order">
					<view class="nav-name">我的订单</view>
					<uni-icons type="forward" size="16"></uni-icons>
				</navigator>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss" scoped>
.personal-container{
	.top-container{
		text-align: center;
		padding: 32rpx 0;
		image{
			width: 200rpx;
			height: 200rpx;
			border-radius: 50%;
		}
		.name{
			padding-top: 16rpx;
			color: #666;
			font-size: 28rpx;
		}
	}
	.order-container{
		padding: 32rpx 120rpx;
		.nav-text{
			display: flex;
			justify-content: space-between;
			align-items: center;
			border: 2rpx solid #ccc;
			padding: 8rpx 16rpx;
			.nav-name{
				color: #333;
				font-size: 32rpx;
			}
		}
	}
}
</style>
