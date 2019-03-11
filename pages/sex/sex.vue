<template>
    <view class="page">
		<view class="item">
			<view  class="item_txt">男</view>
			<image class="item_img" src="/static/gou.png" ></image>
		</view>
		<view class="item">
			<view  class="item_txt">女</view>
			<image class="item_img disnone"  src="/static/gou.png" ></image>
		</view>
		<view class="btn">保存</view>
    </view>
	
</template>

<script>
 
    export default {
        data() {
            return {
				status:false,
            };
        },
        components: {
          
        },
        methods: {
          
        }
    }
</script>

<style lang="scss">
	.item{
		overflow: hidden;
		width: 750upx;
		height: 100upx;
		background: #fff;
		border-bottom:2upx solid #f2f2f2;
		.item_txt{
			float: left;
			font-size: 28upx;
			line-height: 28upx;
			margin:36upx 0 36upx 36upx;
		}
		.item_img{
			float: right;
			width: 40upx;
			height:40upx;
			margin:30upx 32upx 0 0;
		}
	}
	.disnone{
		display: none;
	}
	.disblock{
		display: block
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
		margin-top:148rpx;
	}
</style>
