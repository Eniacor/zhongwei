<template>
	<view>
		<view class="top">
			<view class="title">拼单成功</view>
			<view class="des">预计拼单成功后2天内发货</view>
		</view>
		<view class="address">
			<view class="address_left">
				<image class="left_icon" src="/static/ping6.png"></image>
			</view>
			<view class="address_right">
				<view class="right_title">
					蔡子硕<text>15251130903</text>
				</view>
				<view class="right_des">
					宿迁市 宿城区 西楚大街24-03 宿迁两岸青年创业空间
				</view>
			</view>
		</view>
		<view class="imgs_title">拼单成功</view>
		<view class="imgs">
			<view class="item">
				<image class="img" src="/static/ping4.png"></image>
				<image class="tag" src="/static/ping5.png"></image>
			</view>
			<view class="item">
				<image class="img" src="/static/ping4.png"></image>
			</view>
		</view>
		<view class="goods">
			<image class="goods_left" src=""></image>
			<view class="goods_right">
				<view class="right_title">MacBookPro 2018款 星空灰 32G...</view>
				<view class="right_des">
					<view class="des_num">数量8</view>
					<view class="des_total">实际收款:<text>¥20999</text></view>
				</view>
			</view>
		</view>
		<view class="bottom">
			<view class="btn">返回主页</view>
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
	.top {
		background: #fff;
		padding-top:62upx;
		padding-bottom:62upx;
		padding-left: 60upx;
		.title {
			font-size: 36upx;
			line-height: 36upx;
			color: rgb(34, 34, 34);
		}

		.des {
			margin-top:14upx;
			font-size:28upx;
			line-height:28upx;
			color: rgb(255,158,118);
	
			text {
				color: red;
			}
		}
	}
	.address{
		overflow: hidden;
		height: 156upx;
		background: #fff;
		border-top: 1upx solid #f2f2f2;
		.address_left{
			float:left;
			.left_icon{
				width: 28upx;
				height: 36upx;
				margin-top:68upx;
				margin-left:30upx;
			}
			
		}
		.address_right{
			float:left;
			margin-left: 36upx;
			width: 596upx;
			.right_title{
				font-size:28upx;
				line-height: 28upx;
				margin-top:26upx;
			}
			.right_des{
				font-size:28upx;
				line-height: 34upx;
				margin-top:12upx;
			}
		}
	}
	.imgs_title{
		padding-top:28upx;
		padding-left: 90upx;
		background: #fff;
		margin-top: 15upx;
	}
	.imgs {
		overflow: hidden;
		background: #fff;
		padding: 40upx 90upx;
		.item {
			float: left;
			position: relative;
			height: 96upx;
			.img {
				width: 96upx;
				height: 96upx;
			}
			.tag {
				position: absolute;
				top: 0;
				left: -20upx;
				width: 60upx;
				height: 30upx;
			}

			&:first-child {
				margin-right: 38upx;
			}
		}
	}
	.goods{
		background: #fff;
		padding:12upx 43upx;
		overflow: hidden;
		margin-top:15upx;
		.goods_left{
			float: left;
			width: 140upx;
			height: 140upx;
			border-radius: 10upx;
			background: red;
		}
		.goods_right{
			float: left;
			margin-left:24upx;
			.right_title{
				font-size: 30upx;
				line-height: 30upx;
				margin-top:40upx;
				color: rgb(40,40,40);
			}
			.right_des{
				line-height: 24upx;
				overflow: hidden;
				margin-top:20upx;
				.des_num{
					float: left;
					font_size:24upx;
					line-height: 24upx;
					color: rgb(101,101,101)
				}
				.des_total{
					float: right;
					font_size:24upx;
					line-height: 24upx;
					color: rgb(101,101,101);
					text{
						color: red;
						margin-left: 10upx;
					}
				}
			}
		}
	}
	.bottom{
		margin-top:15upx;
		padding:60upx 0;
		background: #fff;
		.btn{
			width: 690upx;
			height: 92upx;
			line-height: 92upx;
			text-align: center;
			background: #FFD944;
			border-radius: 10upx;
			margin:0 auto;
		}
	}
	
</style>
