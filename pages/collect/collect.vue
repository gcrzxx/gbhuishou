<template>
	<view>
		<view class="form-container">
			<uni-forms ref="valiForm" :modelValue="formData" labelPosition="top">
				<uni-forms-item label="选择回收种类" label-width="150" required="true">
					<picker class="category-picker" mode="selector" :range="array1" @change='categoryChange'>
						<view class="picker-container">
							<view>{{array1[categoryIndex]}}</view>
							<uni-icons type="bottom" size="16"></uni-icons>
						</view>
					</picker>
					<input class="second-input" type="text" placeholder="物品名称" />
				</uni-forms-item>
				<uni-forms-item label="选择预估重量" label-width="150" required="true">
					<picker class="category-picker default-picker" mode="selector" :range="array2" @change='weightChange'>
						<view class="picker-container">
							<view>{{array2[weightIndex]}}</view>
							<uni-icons type="bottom" size="16"></uni-icons>
						</view>
					</picker>
				</uni-forms-item>
				<uni-forms-item label-width="150" label="联系人" required>
					<input class="default-input" type="text">
				</uni-forms-item>
				<uni-forms-item label-width="150" label="联系电话" required>
					<input class="default-input" type="text">
				</uni-forms-item>
				<uni-forms-item label-width="150" label="收货地址" required>
					<input class="default-input" type="text">
				</uni-forms-item>
				<uni-forms-item label="上门时间" label-width="150" required="true">
					<picker class="category-picker default-picker" mode="selector" :range="array3" @change='timeChange'>
						<view class="picker-container">
							<view>{{array3[timeIndex]}}</view>
							<uni-icons type="bottom" size="16"></uni-icons>
						</view>
					</picker>
				</uni-forms-item>
				<!-- 上传图片/视频 -->
				
			</uni-forms>
			<button class="submit-button" type="primary" @click="submit('valiForm')">提交</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				// picker数据
				array1: ['废纸', '塑料', '金属制品', '其他'],
				categoryIndex:0,
				array2: ['5-10斤', '10-15斤', '15-20斤', '20斤以上'],
				weightIndex:1,
				array3: ['1小时以内', '2小时以内', '3小时以内', '4小时以内'],
				timeIndex:1
			}
		},
		methods: {
			// 选择种类切换事件
			categoryChange(event){
				this.categoryIndex = event.detail.value
			},
			weightChange(event){
				this.weightIndex = event.detail.value
			},
			timeChange(event){
				this.timeIndex = event.detail.value
			}
		}
	}
</script>

<style lang="scss" scoped>
 .form-container{
	 padding: 8rpx 24rpx;
	/deep/ .is-required{
		 color: #019946;
	 }
	/deep/ .label-text{
		color: #019946;
		font-size: 32rpx;
	}
	/deep/ .uni-forms-item__content{
		display: flex;
		justify-content: space-between;
	}
	.second-input{
		border: 2rpx solid #019946;
		height: 70rpx;
		padding-left: 20rpx;
		width: 400rpx;
	}
	.default-input{
		border: 2rpx solid #019946;
		height: 70rpx;
		padding-left: 20rpx;
		width: 100%;
	}
 }
 .category-picker{
	 width: 240rpx;
	 border: 2rpx solid #019946;
	 .picker-container{
		 display: flex;
		 align-items: center;
		 justify-content: space-between;
		 padding: 16rpx;
	 }
 }
 .default-picker{
	 width: 100%;
 }
 .submit-button{
	 background-color: #019946;
 }
</style>
