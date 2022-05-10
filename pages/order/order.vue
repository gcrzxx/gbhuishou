<template>
	<view>
		<view class="order">
			<view class="order-list">
				<view class="list-header">
					<view class="list-id">拼团订单ID：54</view>
					<view class="list-state">状态：支付成功</view>
				</view>
				<view class="list-content">
					<view class="list-img">
						<image src="../../static/001.png"></image>
					</view>
					<view class="list-text">
						<view class="text-title">燕之坊五谷杂粮燕麦450克燕之坊五谷杂粮燕麦450克燕之坊五谷杂粮燕麦450克</view>
						<view class="text-description">默认规格 x 1</view>
						<view class="text-price">￥100</view>
					</view>
				</view>
				<view class="list-bottom">
					<view class="list-bottom-left">
						<view>查看拼团</view>
						<view>取消订单</view>
					</view>
					<view class="list-bottom-right">
						共<text>1</text>件商品 实付款<text>￥100</text>
					</view>
				</view>
			</view>
			
			<view class="order-list">
				<view class="list-header">
					<view class="list-id">拼团订单ID：54</view>
					<view class="list-state">状态：支付成功</view>
				</view>
				<view class="list-content">
					<view class="list-img">
						<image src="../../static/001.png"></image>
					</view>
					<view class="list-text">
						<view class="text-title">燕之坊五谷杂粮燕麦450克燕之坊五谷杂粮燕麦450克燕之坊五谷杂粮燕麦450克</view>
						<view class="text-description">默认规格 x 1</view>
						<view class="text-price">￥100</view>
					</view>
				</view>
				<view class="list-bottom">
					<view class="list-bottom-left">
						<view>查看拼团</view>
						<view>取消订单</view>
					</view>
					<view class="list-bottom-right">
						共<text>1</text>件商品 实付款<text>￥100</text>
					</view>
				</view>
			</view>
			
			<view class="order-list">
				<view class="list-header">
					<view class="list-id">拼团订单ID：54</view>
					<view class="list-state">状态：支付成功</view>
				</view>
				<view class="list-content">
					<view class="list-img">
						<image src="../../static/001.png"></image>
					</view>
					<view class="list-text">
						<view class="text-title">燕之坊五谷杂粮燕麦450克燕之坊五谷杂粮燕麦450克燕之坊五谷杂粮燕麦450克</view>
						<view class="text-description">默认规格 x 1</view>
						<view class="text-price">￥100</view>
					</view>
				</view>
				<view class="list-bottom">
					<view class="list-bottom-left">
						<view>查看拼团</view>
						<view>取消订单</view>
					</view>
					<view class="list-bottom-right">
						共<text>1</text>件商品 实付款<text>￥100</text>
					</view>
				</view>
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
	page{
		height: 100%;
		background-color: #f5f4f4;
	}
.order{
	padding: 32rpx 0;
	.order-list{
		padding: 16rpx 32rpx;
		margin-bottom: 40rpx;
		background-color: #ffffff;
		.list-header{
			display: flex;
			justify-content: space-between;
			padding-bottom: 24rpx;
			.list-id{
				font-size: 28rpx;
			}
			.list-state{
				font-size: 24rpx;
				color: #333;
			}
		}
		.list-content{
			display: flex;
			.list-img{
				width: 140rpx;
				height: 140rpx;
				image{
					width: 100%;
					height: 100%;
				}
			}
			.list-text{
				padding-left: 40rpx;
				width: 490rpx;
				.text-title{
					font-size: 32rpx;
					padding-bottom: 8rpx;
					overflow: hidden;
					text-overflow: ellipsis;
					white-space: nowrap;
				}
				.text-description{
					font-size: 28rpx;
					color: #666;
					padding-bottom: 4rpx;
				}
			}
		}
		.list-bottom{
			display: flex;
			justify-content: space-between;
			padding-top: 32rpx;
			.list-bottom-left{
				display: flex;
				view{
					background-color: #4CDB94;
					color: #ffffff;
					font-size: 24rpx;
					padding: 8rpx 12rpx;
					border-radius:12rpx;
					&:nth-of-type(2){
						margin-left: 16rpx;
					}
				}
			}
			.list-bottom-right{
				color: #666;
				text{
					font-size: 32rpx;
					color: #000;
					padding: 0 4rpx;
				}
			}
		}
	}
}
</style>
