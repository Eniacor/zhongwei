<template>
	<view>
		<view class="top">
			<view class="time">23:59:06</view>
			<view class="des">还差<text>1</text>人,赶快邀请好友来拼单吧</view>
			<view class="btn">邀请好友拼单</view>
			<view class="return">返回首页</view>
		</view>
		<view class="bottom">
			<view class="imgs">
				<view class="item">
					<image class="img" src="/static/ping4.png"></image>
					<image class="tag" src="/static/ping5.png"></image>
				</view>
				<view class="item">
					<image class="img" src="/static/ping4.png"></image>
				</view>
			</view>
			<view class="lists">
				<navigator url="/pages/collect/index"  hover-class="none">
					<view class="item">
						<text class="left_txt">订单详情</text>
						<text class="middle_txt">采耳工具套装挖耳朵神器</text>
						<image class="right_img" src="/static/my.png"></image>
					</view>     
				</navigator>
				<navigator url="/pages/collect/index"  hover-class="none">
					<view class="item">
						<text class="left_txt">拼单规则</text>
						<text class="middle_txt">好友拼单,好友拼单,人不满退款</text>
						<!-- <image class="right_img" src="/static/my.png"></image> -->
					</view>     
				</navigator>
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
	.top{
		background: #fff;
		padding-top:8upx;
		padding-bottom:56upx;
		.time{
			width: 190upx;
			height: 44upx;
			line-height: 44upx;
			text-align: center;
			border-radius:6upx;
			background: rgb(242,242,242);
			margin: 0 auto;
		}
		.des{
			margin-top:62upx;
			margin-bottom:30upx;
			font-size: 36upx;
			line-height: 36upx;
			color: #000;
			text-align: center;
			text{
				color:red;
			}
		}
		.btn{
			width: 660upx;
			height: 92upx;
			line-height: 92upx;
			text-align: center;
			font-size:36upx;
			background: rgb(255,217,68);
			color: #000;
			border-radius: 10upx;
			margin:0 auto;
		}
		.return{
			width: 658upx;
			height: 90upx;
			line-height: 92upx;
			text-align: center;
			font-size:36upx;
			border:1upx solid #000;
			color: #000;
			border-radius: 10upx;
			margin:0 auto;
			margin-top:24upx;
		}
	}
	.bottom{
		.imgs{
			overflow: hidden;
			background: #fff;
			margin-top:15upx;
			padding:40upx 260upx;
			.item{
				float: left;
				position: relative;
				height: 96upx;
				.img{
					width: 96upx;
					height: 96upx;
				}
				.tag{
					position: absolute;
					top:0;
					left:-20upx;
					width: 60upx;
					height: 30upx;
				}
				&:first-child{
					margin-right: 38upx;
				}
			}
		}
	}
	.lists{
	    margin-top:16upx;
	    .item{
	        padding:40upx 24upx 40upx 35upx;
	        background: #fff;
	        overflow: hidden;
	        .left_txt{
	            float: left;
	            font-size: 28upx;
	            line-height:28upx;
	            color: rgb(34,34,34);
	        }
			.middle_txt{
				margin-top: 1upx;
				margin-left:110upx;
			    float: left;
			    font-size: 26upx;
				line-height:26upx;
				color: rgb(92,92,92);
			}
	        .right_img{
	            float: right;
	            margin-top: 6upx;
	            width:16upx;
	            height: 27upx;
	            vertical-align:bottom;
	        }
	    }
	}
</style>
