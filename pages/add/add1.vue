<template>
	<view>
		<view class="hello">欢迎您</view>
		<view class="hello">来到中微直供</view>
		<image class="img" src="/static/add1.png"></image>
		<view class="btn">登录</view>
		<view class="regist">注册</view>
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
	page{
		background: #fff;
	}
	.hello{
		font-size: 50upx;
		line-height: 50upx;
		color: rgb(79, 79, 79);
		&:first-child{
			margin-top: 84upx;
			margin-left: 58upx;
		}
		&:nth-child(2){
			margin-top: 14upx;
			margin-left: 58upx;
		}
	}
	.img{
		display: block;
		width:576upx;
		height: 552upx;
		margin: 0 auto;
		margin-top:100upx;
		margin-bottom:130upx;
	}
	.btn{
		width: 630upx;
		height: 102upx;
		border-radius: 10upx;
		background: rgb(255,217,68);
		margin:0 auto;
		line-height: 102upx;
		text-align: center;
		font-size: 28upx;
	}
	.regist{
		font-size: 28upx;
		line-height: 102upx;
		text-align: center;
		color: rgb(161,178,255);
	}
</style>
