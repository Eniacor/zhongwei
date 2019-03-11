<template>
	<view>
		<view class="lists">
			<navigator url="/pages/address/index"  hover-class="none">
				<view class="item">
					<text class="left_txt">实名认证</text>
					<image class="right_img" src="/static/my.png"></image>
				</view>   
			</navigator>
			<navigator url="/pages/address/index"  hover-class="none">
				<view class="item">
					<text class="left_txt">修改密码</text>
					<image class="right_img" src="/static/my.png"></image>
				</view>   
			</navigator>
			<navigator url="/pages/address/index"  hover-class="none">
				<view class="item">
					<text class="left_txt">收获地址</text>
					<image class="right_img" src="/static/my.png"></image>
				</view>   
			</navigator>
			<navigator url="/pages/address/index"  hover-class="none">
				<view class="item">
					<text class="left_txt">切换账号</text>
					<image class="right_img" src="/static/my.png"></image>
				</view>   
			</navigator>
			<navigator url="/pages/address/index"  hover-class="none">
				<view class="item">
					<text class="left_txt">检查更新</text>
					<image class="right_img" src="/static/my.png"></image>
				</view>   
			</navigator>
		</view>
		<view class="btn">登录账号</view>
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
.lists{
    .item{
        padding:35upx 35upx;
        background: #fff;
        overflow: hidden;
        .left_txt{
            float: left;
            font-size: 30upx;
            line-height: 30upx;
            color: rgb(51,51,51);
            margin-left: 23upx;
        }
        .right_img{
            float: right;
            margin-top: 5upx;
            width:16upx;
            height: 27upx;
            vertical-align:bottom;
        }
    }
}
.btn{
	width: 690upx;
	height: 88upx;
	line-height: 88upx;
	font-size: 30upx;
	color: #000;
	text-align: center;
	border-radius: 10upx;
	background: #FFD944;
	margin:0 auto;
	margin-top:240upx;
}
</style>
