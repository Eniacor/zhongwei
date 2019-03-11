<template>
	<view>
		<image class="banner" src="/static/service1.png"></image>
		<view class="content">
			<view class="content_tel">
				<image class="tel_img" src="/static/service2.png"></image>
				<text class="tel_txt">客服电话：</text>
				<text class="tel_val">15361314895</text>
			</view>
			<view class="content_qq">
				<image class="qq_img" src="/static/service3.png"></image>
				<text class="qq_txt">QQ号码：</text>
				<text class="qq_val">1011011</text>
			</view>
			<view class="des">
				感谢您的支持，如果您有相关问题，请联系中微直供客服，
				我们将对您的问题作出反馈
			</view>
		</view>
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
	.banner{
		display: block;
		width: 700upx;
		height: 376upx;
		margin:0 auto;
	}
	.content{
		width: 700upx;
		height:740upx;
		background: #fff;
		margin:0 auto;
		border-bottom-left-radius: 10upx;
		border-bottom-right-radius: 10upx;
		.content_tel{
			overflow: hidden;
			.tel_img{
				float: left;
				width: 64upx;
				height: 64upx;
				margin-top:112upx;
				margin-left: 130upx;
			}
			.tel_txt{
				float: left;
				font-size: 30upx;
				line-height: 30upx;
				color: rgb(51,51,51);
				margin-top:128upx;
				margin-left: 16upx;
			}
			.tel_val{
				float: left;
				font-size: 30upx;
				line-height: 30upx;
				color: rgb(51,51,51);
				margin-top:128upx;
			}
		}
		.content_qq{
			overflow: hidden;
			margin-bottom:78upx;
			.qq_img{
				float: left;
				width: 64upx;
				height: 64upx;
				margin-top:33upx;
				margin-left: 130upx;
			}
			.qq_txt{
				float: left;
				font-size: 30upx;
				line-height: 30upx;
				color: rgb(51,51,51);
				margin-top:46upx;
				margin-left: 16upx;
			}
			.qq_val{
				float: left;
				font-size: 30upx;
				line-height: 30upx;
				color: rgb(51,51,51);
				margin-top:46upx;
			}
		}
		.des{
			
			width: 572upx;
			height: 178upx;
			background: rgb(242, 242, 242);
			margin: 0 auto;
			border-radius: 10upx;
			padding:80upx 50upx 0 50upx;
			font-size: 29upx;
			line-height: 40upx;
		}
	}
</style>
