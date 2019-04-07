<template>
	<view>
		<view class="bar">
			<view class="left">
				<view class="shop">
					<image class="shop_img" src="/static/shop.png" ></image>
					<view class="shop_title">店铺</view>
				</view>
				<view class="cart">
					<image class="cart_img" src="/static/cart.png" ></image>
					<view class="cart_title">购物车</view>
					<view class="cart_tag">{{num}}</view>
				</view>
			</view>
			<view class="right">
				<view class="right_price">分享赚</view>
				<view class="right_discount">立赚￥{{zhuan}}</view>
			</view>
			<view class="middle">
				<view class="middle_price">立即购买</view>
				<view class="middle_discount">立省￥{{sheng}}</view>
			</view>
			<view class="line"></view>
		</view>
	</view>
</template>

<script>
	export default {
		props: {
			num: {
				type: Number,
				default:0
			},
			sheng: {
				type: Number,
				default:0
			},
			zhuan: {
				type: Number,
				default:0
			}
		}, 
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
	.bar{
		width:100%;
		height:98upx;
		position: fixed;
		bottom:0;
		border-top: 1upx solid #f1f1f1;
		overflow: hidden;
		background: #fff;
		.left{
			float: left;
			.shop{
				float: left;
				.shop_img{
					width:40upx;
					height:42upx;
					margin-top: -16upx;
					margin-left:14upx;
				}
				.shop_title{
					font-size:16upx;
					line-height:16upx;
					color: rgb(159,159,159);
					margin-top: -12upx;
					margin-left:16upx;
				}
			}
			.cart{
				float: left;
				position: relative;
				.cart_img{
					width:42upx;
					height:44upx;
					vertical-align: bottom;
					margin-top: 26upx;
					margin-left:14upx;
				}
				.cart_title{
					font-size:14upx;
					line-height:12upx;
					color: rgb(159,159,159);
					margin-top: 4upx;
					margin-left:11upx;
				}
				.cart_tag{
					position: absolute;
					top:16upx;
					left:44upx;
					width:34upx;
					height:34upx;
					font-size: 12upx;
					line-height: 34upx;
					text-align: center;
					border-radius: 50%;
					background:#F12C20;
					color:#fff;
				}
			}
		}
		.line{
			margin-top:8upx;
			float: right;
			width: 2upx;
			height: 84upx;
			background:#dcdcdc;
		}
		.middle{
			float: right;
			width: 270upx;
			height: 98upx;
			.middle_price{
				text-align: center;
				font-size: 24upx;
				line-height: 24upx;
				color: rgb(51,51,51);
				margin-top: 28upx;
			}
			.middle_discount{
				margin-top:8upx;
				text-align: center;
				font-size:14upx;
				line-height:12upx;
				color: rgb(51,51,51);
			}
		}
		.right{
			float: right;
			width: 290upx;
			height: 98upx;
			background:#D41C1C; 
			.right_price{
				text-align: center;
				font-size: 24upx;
				line-height: 24upx;
				color: #fff;
				margin-top: 28upx;
			}
			.right_discount{
				margin-top:8upx;
				text-align: center;
				font-size:14upx;
				line-height:12upx;
				color: #fff;
			}
		}
	}
	
</style>

