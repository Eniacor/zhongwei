<template>
	<view>
		<view class="card_title">为保证您的资金安全，请绑定账户本人的银行卡</view>
		<view class="card_content">
			<view class="content_lable">卡号</view>
			<input class="content_name" value="6217 0013 2000 3414 614" />
		</view>
		<view class="card_name">
			<image class="name_icon" />
			<text  class="name_txt">中国建设银行储蓄卡</text>
		</view>
		<navigator url="/pages/mycard/mycard2"  hover-class="none">
			<view class="card_btn">下一步</view>
		</navigator>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		},
		components: {
		},
	}
</script>

<style lang="scss">
	.card_title{
		margin-top:54upx;
		margin-left:35upx;
		font-size: 28upx;
		line-height: 28upx;
		color: #000;
	}
	.card_content{
		width: 686upx;
		height: 72upx;
		margin: 0 auto;
		background:rgba(195,195,195,.24);
		border-radius: 14upx;
		overflow: hidden;
		margin-top:53rpx;
		.content_lable{
			float: left;
			font-size: 30upx;
			line-height:30upx;
			color:rgb(40,40,40);
			margin:20upx 0 0 26upx;
		}
		.content_name{
			float: left;
			font-size: 30upx;
			line-height:30upx;
			margin:8upx 0 0 60upx;
		}
	}
	.card_name{
		margin-top:21upx;
		margin-left:52upx;
		.name_icon{
			width: 40upx;
			height: 40upx;
			border-radius: 50%;
			background:#FFD944;
			vertical-align: middle;
		}
		.name_txt{
			font-size: 20upx;
			line-height: 20upx;
			color: rgb(102,102,102);
			margin-left: 22upx;
		}
	}
	.card_btn{
		width: 682upx;
		height: 80upx;
		background: #FFD944;
		border-radius: 10upx;
		font-size: 30upx;
		line-height:80upx;
		text-align: center;
		margin: 0 auto;
		margin-top:90upx;
	}
	.popup_content{
		width: 624upx;
		height: 582upx;
		background: #fff;
		border-radius: 16upx;
		.content_title{
			font-size: 36upx;
			line-height: 36upx;
			color:#000;
			text-align: center;
			margin-top: 48upx;
			margin-bottom: 48upx;
		}
		.content_content{
			padding:0 44upx;
			.content_item{
				font-size: 30upx;
				line-height: 40upx;
				color:rgb(102,102,102);
			}
		}
		.content_bottom{
			border-top: 1upx solid #f2f2f2;
			font-size: 36upx;
			line-height: 100upx;
			text-align: center;
			margin-top:30upx;
		}
	}
</style>
