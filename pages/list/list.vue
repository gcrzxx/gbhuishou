<template>
	<view>
		<view class="list-container">
			<navigator url="/pages/details/details">
				<view class="item-container">
					<view class="item-left">
						<image src="../../static/001.png"></image>
					</view>
					<view class="item-right">
						<view class="item-title">新闻标题一</view>
						<view class="item-content">新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容</view>
					</view>
				</view>
			</navigator>
			<navigator url="/pages/details/details">
				<view class="item-container">
					<view class="item-left">
						<image src="../../static/001.png"></image>
					</view>
					<view class="item-right">
						<view class="item-title">新闻标题一</view>
						<view class="item-content">新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容</view>
					</view>
				</view>
			</navigator>
			<navigator url="/pages/details/details">
				<view class="item-container">
					<view class="item-left">
						<image src="../../static/001.png"></image>
					</view>
					<view class="item-right">
						<view class="item-title">新闻标题一</view>
						<view class="item-content">新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容</view>
					</view>
				</view>
			</navigator>
			<navigator url="/pages/details/details">
				<view class="item-container">
					<view class="item-left">
						<image src="../../static/001.png"></image>
					</view>
					<view class="item-right">
						<view class="item-title">新闻标题一</view>
						<view class="item-content">新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容新闻内容</view>
					</view>
				</view>
			</navigator>
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
.list-container{
	padding: 24rpx;
	.item-container{
		display: flex;
		justify-content: space-between;
		padding: 24rpx 0;
		.item-left{
			width: 30%;
			image{
				width: 100%;
				height: 100%;
			}
		}
		.item-right{
			width: 60%;
			.item-title{
				font-size: 32rpx;
				font-weight: 700;
			}
			.item-content{
				font-size: 28rpx;
				color: #666;
				padding-top: 16rpx;
				display: -webkit-box;
				overflow: hidden;
				text-overflow: ellipsis;
				-webkit-line-clamp: 2;
				-webkit-box-orient: vertical;
			}
		}
	}
}
</style>
