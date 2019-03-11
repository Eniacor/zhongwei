<template>
	<view>
		<view class="nickname">
			<textarea
				placeholder="给自己取一个郎朗上口的昵称吧～"
				class="custom_textarea"/>
			<view class="tip">最多10个字符</view>
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
.nickname{
    position: relative;
    padding:50upx 35upx 50upx 35upx;
    background: #fff;
    .custom_textarea{
        width: 680upx!important;
        height: 200upx!important;
        font-size: 30upx;
        line-height: 30upx;
        color:#707070;
    }
    .tip{
        position: absolute;
        bottom: 20upx;
        right:38upx;
        font-size: 24upx;
        line-height: 24upx;
        color:#999999;
    }
}
.btn{
    width: 684upx;
    height: 82upx;
    background: #C3C3C3;
    color:rgb(51, 51, 51);
    line-height: 82upx;
    text-align: center;
    margin:0 auto;
    border-radius: 10upx;
    margin-top:60upx;
}
</style>
