<template>
	<view>
		<navigator url="/pages/address/index"  hover-class="none">
			<view class="user">
				<text class="left_txt">请为您的账号187***5726修改密码</text>
				<image class="right_img" src="/static/my.png"></image>
			</view>   
		</navigator>
		<navigator url="/pages/address/index"  hover-class="none">
			<view class="password1">
				<text class="left_txt">旧密码</text>
				<!-- <image class="right_img" src="/static/my.png"></image> -->
			</view>   
		</navigator>
		<navigator url="/pages/address/index"  hover-class="none">
			<view class="password2">
				<text class="left_txt">请输入旧密码</text>
				<input class="middle_input" placeholder="52289Y" />
				<image class="right_img" src="/static/password2.png"></image>
			</view>   
		</navigator>
		<navigator url="/pages/address/index"  hover-class="none">
			<view class="password1">
				<text class="left_txt">新密码</text>
				<!-- <image class="right_img" src="/static/my.png"></image> -->
			</view>   
		</navigator>
		<navigator url="/pages/address/index"  hover-class="none">
			<view class="password2">
				<text class="left_txt">请输入新密码</text>
				<input class="middle_input" placeholder="********" />
				<image class="right_img" src="/static/password1.png"></image>
			</view>   
		</navigator>
		<navigator url="/pages/address/index"  hover-class="none">
			<view class="password2">
				<text class="left_txt">请输入新密码</text>
				<input class="middle_input" placeholder="********" />
				<image class="right_img" src="/static/password1.png"></image>
			</view>   
		</navigator>
		<view class="btn">保存新密码</view>
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
	
.user{
	padding:86upx 35upx 86upx 78upx;
	background: #fff;
	overflow: hidden;
	margin-top:19upx;
	.left_txt{
		float:left;
	    font-size:30upx;
	    line-height:30upx;
	    color: rgb(51,51,51);
	}
	.right_img{
	    float: right;
	    margin-top: 5upx;
	    width:16upx;
	    height: 27upx;
	    vertical-align:bottom;
	}
}
.password1{
	padding:30upx 35upx 12upx 24upx;
	overflow: hidden;
	.left_txt{
		float:left;
	    font-size:28upx;
	    line-height:28upx;
	    color: rgb(51,51,51);
	}
	.right_img{
	    float: right;
	    margin-top: 5upx;
	    width:16upx;
	    height: 27upx;
	    vertical-align:bottom;
	}
}
.password2{
	padding:35upx 26upx 35upx 24upx;
	background: #fff;
	overflow: hidden;
	.left_txt{
		float:left;
	    font-size:30upx;
	    line-height:30upx;
	    color: rgb(38,38,38);
		margin-top:10upx;
	}
	.middle_input{
		float: left;
		text-align: right;
		font-size:30upx;
		margin-left:115upx;
	}
	.right_img{
	    float: right;
	    margin-top:16upx;
	    width:40upx;
	    height: 20upx;
	    vertical-align:bottom;
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
