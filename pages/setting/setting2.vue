<template>
	<view>
		<image class="img" src="/static/setting1.png"></image>
		<view class="notice">认证成功</view>
		<view class="btn">去逛逛</view>
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
	.btn{
		width: 690upx;
		height: 90upx;
		text-align: center;
		line-height: 90upx;
		color:#fff;
		border-radius: 10upx;
		background: #4280F2;
		margin:0 auto;
		margin-top:354upx;
	}
</style>
