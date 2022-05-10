<template>
	<view>
		<view class="login-container">
			<button size="mini" open-type="getPhoneNumber" @getphonenumber="getPhone">点击登录</button>
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
			getPhone(event){
				console.log(event);
			}
		}
	}
</script>

<style lang="scss" scoped>
.login-container{
	button{
		background-color: #48E67A;
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		width: 300rpx;
		padding: 8rpx 0;
	}
}
</style>
