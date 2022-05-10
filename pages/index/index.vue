<template>
	<view class="wrapper">
		<view class="top-state"></view>
		<view class="public-header">项目</view>
		<view class="swiper-container">
			<!-- <swiper :circular='true'>
				<swiper-item>
					<image src="../../static/001.png"></image>
				</swiper-item>
				<swiper-item>
					<image src="../../static/001.png"></image>
				</swiper-item>
			</swiper> -->
			<image src="../../static/001.png"></image>
		</view>
		<!-- 内容区 -->
		<view class="container">
			<view class="top-area">
				<view class="top-area-list" @click="toCollect">
					<uni-icons type="shop" size="50" color="#4CDB94"></uni-icons>
					<view class="top-text">金属类回收</view>
				</view>
				<view class="top-area-list" @click="getAddress">
					<uni-icons type="shop" size="50" color="#4CDB94"></uni-icons>
					<view class="top-text">塑料类回收</view>
				</view>
				<view class="top-area-list" @click="toLogin">
					<uni-icons type="shop" size="50" color="#4CDB94"></uni-icons>
					<view class="top-text">旧电器回收</view>
				</view>
				<view class="top-area-list">
					<uni-icons type="shop" size="50" color="#4CDB94"></uni-icons>
					<view class="top-text">其他物品回收</view>
				</view>
			</view>
		</view>
		<!-- 底部区域 -->
		<view class="container2">
			<view class="bottom-area">
				<view class="bottom-title">工博回收</view>
				<view class="bottom-container">
					<view class="bottom-list" @click="toIntroduce">
						<view class="list-title">积分商城</view>
						<view class="list-description">更多免费福利</view>
					</view>
					<view class="bottom-list" @click="toList">
						<view class="list-title">闲置商城</view>
						<view class="list-description">更多开心捡漏</view>
					</view>
					<view class="bottom-list">
						<button open-type="contact">
							<text>服务咨询</text>
							<text>专业客服解答</text>
						</button>
					</view>
					<view class="bottom-list" @click="call">
						<view class="list-title">热线电话</view>
						<view class="list-description">专业客服解答</view>
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
			// 客服电话
			call(){
				uni.makePhoneCall({
					phoneNumber:'18362986576'
				})
			},
			// 跳转回收物品页面
			toCollect(){
				uni.navigateTo({
					url:'../collect/collect'
				})
			},
			toIntroduce(){
				uni.navigateTo({
					url:'../introduce/introduce'
				})
			},
			// 前往列表页
			toList(){
				uni.navigateTo({
					url:'../list/list'
				})
			},
			getAddress(){
				uni.chooseLocation({
					success: (res) => {
						console.log(res.address);
					}
				})
			},
			toLogin(){
				uni.navigateTo({
					url:"../login/login"
				})
			}
		}
	}
</script>

<style lang="scss">
	.top-state{
		height: var(--status-bar-height);
		width: 750rpx;
	}
	.public-header{
		position: fixed;
		width: 750rpx;
		height: 120rpx;
		background-image: linear-gradient(to right,#41b7fd,#734df0);
		top: 0;
		padding-top: var(--status-bar-height);
		display: flex;
		justify-content: center;
		align-items: center;
		color: #ffffff;
	}
	.wrapper{
		position: relative;
		height: 100%;
	}
	page{
		height: 100%;
		background-color: #eae0e0;
	}
	.swiper-container{
		// swiper{
		// 	height: 460rpx;
		// }
		height: 460rpx;
		image{
			width: 750rpx;
			height: 100%;
			border-bottom-left-radius: 60rpx;
			border-bottom-right-radius: 60rpx;
		}
	}
	// 内容区
	.container{
		background: #fff;
		position: absolute;
		top: 400rpx;
		left: 32rpx;
		right: 32rpx;
		border-top-left-radius: 20rpx;
		border-top-right-radius: 20rpx;
		.top-area{
			display: flex;
			justify-content: space-between;
			padding: 20rpx;
			.top-area-list{
				text-align: center;
				.top-text{
					font-size: 24rpx;
					color: #666;
					padding-top: 8rpx;
				}
			}
		}
	}
	.container2{
		background: #fff;
		position: absolute;
		top: 600rpx;
		left: 32rpx;
		right: 32rpx;
		border-top-left-radius: 20rpx;
		border-top-right-radius: 20rpx;
		.bottom-area{
			padding: 20rpx;
			.bottom-title{
				font-size: 36rpx;
				padding-bottom: 20rpx;
			}
			.bottom-container{
				display: flex;
				flex-wrap: wrap;
				justify-content: space-between;
				.bottom-list{
					width: 48%;
					text-align: center;
					border-radius: 20rpx;
					padding: 24rpx 0;
					color: #fff;
					.list-description{
						font-size: 28rpx;
						padding-top: 4rpx;
					}
				}
				.bottom-list{
					&:nth-of-type(1){
						background-image: linear-gradient(to right,#cccccc,#C17DF5);
					}
					&:nth-of-type(2){
						background-image: linear-gradient(to right,#cccccc,#FE764E);
					}
					&:nth-of-type(3){
						margin-top: 20rpx;
						padding: 0;
						button{
							height: 64px;
							background-image: linear-gradient(to right,#cccccc,#FE8087);
							border-radius: 20rpx;
							color: #ffffff;
							font-size: 32rpx;
							display: flex;
							flex-direction: column;
							text{
								&:first-child{
									height: 50rpx;
									padding-top: 8rpx;
								}
								&:last-child{
									font-size: 28rpx;
								}
							}
						}
					}
					&:nth-of-type(4){
						background-image: linear-gradient(to right,#cccccc,#48E67A);
						margin-top: 20rpx;
					}
				}
			}
		}
	}
</style>
