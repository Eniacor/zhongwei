<template>
	<view>
		<view class="address_title">所在区域</view>
		<view class="address">
			<view class="address_left">
				<text class="left_txt">江苏省</text>
				<text class="left_txt">盐城市</text>
				<text class="left_txt">亭湖区</text>
			</view>
			<image class="right_img" src="/static/my.png"></image>
		</view>
		<view class="pictures_title">请拍摄并上传你的身份证照片</view>
		<view class="pictures">
			<view class="item">
				<image class="img" src="/static/author1.png"></image>
				<view class="btn">拍摄正面</view>
			</view>
			<view class="item">
				<image class="img" src="/static/author2.png"></image>
				<view class="btn">拍摄正面</view>
			</view>
		</view>
		<view class="register">
			<uni-icon size="24" type="checkbox-filled" color="#09BB07"></uni-icon><text>注册即表示您已阅读并同意服务条款</text>
		</view>
		<view class="btn2">下一步</view>
		<view class="second">稍后认证</view>
	</view>
</template>

<script>
	import uniIcon from '../../components/uni-icon.vue'
	export default {
		data() {
			return {
			
			};
		},
		components: {
		    uniIcon
		},
	}
</script>

<style lang="scss">
	.address_title {
		width: 100%;
		background: #fff;
		padding: 30upx 30upx;
		font-size: 30upx;
		line-height: 30upx;

	}

	.address {
		border-top: 1upx solid #f2f2f2;
		padding: 52upx 28upx 42upx 0;
		background: #fff;
		overflow: hidden;

		.address_left {
			float: left;
			.left_txt {
				font-size: 28upx;
				line-height: 28upx;
				color: rgb(51, 51, 51);
				margin-left: 90upx;
			}
		}

		.right_img {
			float: right;
			margin-top: 5upx;
			width: 16upx;
			height: 27upx;
			vertical-align: bottom;
		}
	}

	.pictures_title {
		font-size: 30upx;
		line-height: 30upx;
		padding-top: 29upx;
		padding-left: 30upx;
		background: #fff;
		margin-top: 15upx;
	}

	.pictures {
		overflow: hidden;
		background: #fff;
		padding: 30upx 30upx 30upx 30upx;

		.item {
			float: left;

			.img {
				width: 324upx;
				height: 224upx;
			}

			.btn {
				width: 324upx;
				height: 60upx;
				background: #4280F2;
				font-size: 28 upx;
				line-height: 60upx;
				text-align: center;
				color: #fff;
				border-bottom-left-radius: 10upx;
				border-bottom-right-radius: 10upx;
			}

			&:first-child {
				margin-right: 42upx;
			}
		}
	}

	.register {
		margin-top:46upx;
		margin-left:22upx;
		text{
			font-size:26upx;
			line-height:26upx;
			margin-left: 14upx;
		}
	}

	.btn2 {
		width: 610upx;
		height: 92upx;
		line-height: 92upx;
		font-size: 36upx;
		color: #000;
		text-align: center;
		border-radius: 10upx;
		background:#FFD944;
		margin: 0 auto;
		margin-top:160upx;
	}
	.second{
		margin-top:44upx;
		font-size: 32upx;
		line-height:32upx;
		text-align:center;
		color:#7389F3;
	}
</style>
