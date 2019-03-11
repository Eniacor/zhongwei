<template>
	<view>
		<view class="ll">请拍摄并上传你的身份证照片</view>
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
		<view class="content">
			<view class="title">拍摄身份证要求</view>
			<view class="des">大陆公民持有的本人有效二代身份证；</view>
			<view class="des">拍摄时确保身份证<text>边框完整，字体清晰，亮度均匀；</text></view>
			<image class="img" src="/static/author3.png"></image>
		</view>
		<view class="btn">身份认证</view>
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
	.ll{
		font-size: 30upx;
		line-height: 30upx;
		padding-top:29upx;
		padding-left: 30upx;
		background: #fff;
	}
	.pictures{
		overflow: hidden;
		background: #fff;
		padding:30upx 30upx 30upx 30upx;
		.item{
			float: left;
			.img{
				width:324upx;
				height:224upx;
			}
			.btn{
				width: 324upx;
				height: 60upx;
				background:#4280F2;
				font-size: 28 upx;
				line-height: 60upx;
				text-align: center;
				color: #fff;
				border-bottom-left-radius: 10upx;
				border-bottom-right-radius: 10upx;
			}
			&:first-child{
				margin-right: 42upx;
			}
		}
	}
	.content{
		padding-top:40upx;
		background: #fff;
		margin-top:30upx;
		.title{
			padding:38upx 0 30upx 30upx;
			font-size: 30upx;
			line-height: 30upx;
			color:rgb(27, 27, 32);
		}
		.des{
			padding-left: 30upx;
			font-size: 26upx;
			line-height: 26upx;
			color:rgb(145, 145, 145);
			margin-bottom: 10upx;
		}
		.img{
			width: 750upx;
			height: 204upx;
			margin-top:60upx;
			vertical-align: bottom;
		}
	}
	.btn{
		width: 690upx;
		height: 88upx;
		line-height: 88upx;
		font-size: 36upx;
		color: #fff;
		text-align: center;
		border-radius: 10upx;
		background: rgb(193, 198, 197);
		margin:0 auto;
		margin-top:56upx;
	}
</style>
