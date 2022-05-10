<template>
	<view>
		<view class="details-container">
			<view class="choose-button">
				<view class="introduce" :class="actived ? 'button-active' : '' " @click="changeButton">知识介绍</view>
				<view class="news-list" :class="actived2 ? 'button-active' : '' " @click="changeButton2">新闻中心</view>
			</view>
			<view class="container1" v-if="actived">
				<uni-collapse accordion>
					<uni-collapse-item title="标题一" open="true">
						<view class="details-text">手风琴效果同时只会保留一个组件的打开状态，其余组件会自动关闭。</view>
					</uni-collapse-item>
					<uni-collapse-item title="标题二">
						<view class="details-text">手风琴效果同时只会保留一个组件的打开状态，其余组件会自动关闭。</view>
					</uni-collapse-item>
					<uni-collapse-item title="标题三">
						<view class="details-text">手风琴效果同时只会保留一个组件的打开状态，其余组件会自动关闭。</view>
					</uni-collapse-item>
					<uni-collapse-item title="标题四">
						<view class="details-text">手风琴效果同时只会保留一个组件的打开状态，其余组件会自动关闭。</view>
					</uni-collapse-item>
				</uni-collapse>
			</view>
			
			<view class="list-container" v-if="actived2">
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
	</view>
</template>

<script>
	export default {
		data() {
			return {
				actived:true,
				actived2:false
			}
		},
		methods: {
			changeButton(){
				this.actived = true
				this.actived2 = false
			},
			changeButton2(){
				this.actived2 = true
				this.actived = false
			}
		}
	}
</script>

<style lang="scss" scoped>
.details-container{
	.choose-button{
		display: flex;
		margin: 48rpx auto;
		width: fit-content;
		border: 2rpx solid #4cdb94;
		font-size: 28rpx;
		.introduce,.news-list{
			padding: 12rpx 24rpx;
		}
		.button-active{
			background-color: #4cdb94;
			color: #ffffff;
		}
	}
	.details-text{
		padding: 16rpx 32rpx;
	}
}

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
