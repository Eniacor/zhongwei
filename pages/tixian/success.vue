<template>
	<view>
		<image class="img" src="/static/tijiao.png"></image>
		<view class="des">提现申请已提交，等待人工审核</view>
		<view class="date">2019-11-11 15:11:28</view>
		<view class="time">预计到账时间：11月11日</view>
		<view class="btn">完成</view>
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
		width: 227upx;
		height: 192upx;
		margin: 0 auto;
		margin-top:145upx;
		margin-bottom:70upx;
	}
	.des{
		font-size: 32upx;
		line-height: 32upx;
		color: rgb(51,51,51);
		margin-bottom:21upx;
		text-align: center;
	}
	.date{
		margin-bottom:25upx;
		font-size:24upx;
		line-height:24upx;
		color: rgb(102,102,102);
		text-align: center;
	}
	.time{
		margin-bottom:119upx;
		font-size:24upx;
		line-height:24upx;
		color: rgb(102,102,102);
		text-align: center;
	}
	.btn{
		width:470upx;
		height:104upx;
		margin:0 auto;
		font-size: 34upx;
		line-height:104upx;
		color: rgb(0, 0, 0);
		text-align: center;
		border-radius: 50upx;
		background: #FFD944;
	}
</style>
