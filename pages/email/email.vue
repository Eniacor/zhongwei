<template>
	<view>
		<view class="top">
			<view class="top_title">填写邮箱地址</view>
			<input class="top_input"/>
		</view>
		<view class="btn">保存</view>
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
.top{
    height: 207rpx;
    background: #fff;
    padding:46rpx 32rpx;
    font-size: 30rpx;
    color:#A3A3A3;
    .top_input{
        margin-top:60rpx;
        width: 686rpx;
        height: 72rpx;
        border-radius: 20rpx;
        background:#F1F1F1; 
        color:rgb(51, 51, 51);
        padding-left:30rpx;
    }
}
.btn{
    width: 684rpx;
    height: 82rpx;
    background:#FFD944;
    color:rgb(51, 51, 51);
    line-height: 82rpx;
    text-align: center;
    margin:0 auto;
    border-radius: 10rpx;
    margin-top:58rpx;
}
</style>
