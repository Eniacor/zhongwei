<template>
	<view>
		<image class="img" src="/static/setting2.png"></image>
		<view class="notice">认证失败</view>
		<view class="des">您的身份证照片不符合要求，请重新认证</view>
		<view class="btn">重新认证</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
	.img{
		display: block;
		width: 326upx;
		height: 249upx;
		margin:0 auto;
		margin-top:180upx;
	}
	.notice{
		margin-top:70upx;
		font-size: 40upx;
		line-height: 40upx;
		text-align: center;
	}
	.des{
		margin-top:76upx;
		font-size: 24upx;
		line-height:24upx;
		text-align: center;
	}
	.btn{
		width: 690upx;
		height: 90upx;
		text-align: center;
		line-height: 90upx;
		color:#fff;
		border-radius: 10upx;
		background: #4280F2;
		margin:0 auto;
		margin-top:256upx;
	}
</style>
