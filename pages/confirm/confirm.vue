<template>
	<view>
		<view class="type" @click="onPostPopup">
			<text class="type_left">我的发布</text>
			<image class="type_right" src="/static/my.png"></image>
			<text class="type_middle">快递 免邮</text>
		</view>
		<view class="goods">
			<view class="goods_left">
				<image class="goods_img"></image>
			</view>
			<view class="goods_right">
				<view class="right_title">小米 红色6 Pro 全网通手机 双卡双...</view>
				<view class="right_des">规格4+32G 颜色：巴黎蓝</view>
				<view class="right_res">库存322件</view>
				<view class="right_price">￥118</view>
				<view class="right_count">
					<view class='stepper'>
						<view class='subtract'>-</view>
						<input class='count' value="0"></input>
						<view class='add'>+</view>
					</view>
				</view>
			</view>
		</view>
		<view class="address">
			<view class="img">
				<uni-icon size="28" type="plus" color="#696969"></uni-icon>
			</view>
			<view class="txt">
				添加收货地址
			</view>
		</view>

		<view class="message">
			<view class="message_left">我的发布</view>
			<view class="message_middle">
				<textarea class="middle_txt" value="" placeholder="选填:填写内容已和卖家协商确认" />
				</view>
			<image class="message_right" src="/static/clear.png"></image>
		</view>
		<view class="discount">
			<view class="discount_left">我的优惠券</view>
			<view class="discount_right">暂无可用优惠券</view>
		</view>
		
		<view class="money">
			<view class="item">
				<view class="item_left">
					商品金额
				</view>
				<view class="item_right">
					￥118.00
				</view>
			</view>
			<view class="item">
				<view class="item_left">
					运费
				</view>
				<view class="item_right">
					+￥0.00
				</view>
			</view>
			<view class="total">
				<view class="total_right">
					合计：<text class="num">￥118.00</text>
				</view>
				<view class="total_count">
					共<text class="num">1</text>件，
				</view>
			</view>
			<view class="bottom">
				<view class="bottom_left">
					实付款：<text class="num">￥118</text>
				</view>
				<view class="bottom_right" @click="onPaymentPopup">
					立即支付
				</view>
			</view>
		</view>
		
		<view class="post">
			<uni-popup :show="showPopupPost" type="bottom" v-on:hidePopup="hidePopup">
				<view class="post_content">
					<view class="content_title">
						<view class="title">配送方式</view>
						<view class="clear"  @click="hidePopup">
							<uni-icon size="34" type="closeempty" color="#696969"></uni-icon>
						</view>
					</view>
					<view class="content_item">
						<view class="item_title">快递 免邮</view>
						<view class="delete">
							<uni-icon size="24" type="checkbox-filled" color="#D41C1C"></uni-icon>
						</view>
					</view>
				</view>
			</uni-popup>
		</view>
		<view class="pay">
			<uni-popup :show="showPopupPayment" type="bottom" v-on:hidePopup="hidePopup">
				<view class="post_content">
					<view class="content_title">
						<view class="title">请选择支付方式</view>
						<view class="clear"  @click="hidePopup">
							<uni-icon size="34" type="closeempty" color="#696969"></uni-icon>
						</view>
					</view>
					<view class="content_content">
						<view class="content_item">
							<image class="item_left"></image>
							<view class="item_middle">
								<view class="middle_title">支付宝支付</view>
								<view class="middle_des">扫二维码领取红包支付更优惠</view>
							</view>
							<view class="delete">
								<uni-icon size="24" type="checkbox-filled" color="#D41C1C"></uni-icon>
							</view>
						</view>
						<view class="content_item">
							<image class="item_left"></image>
							<view class="item_middle">
								<view class="middle_title">微信支付</view>
								<view class="middle_des">扫二维码领取红包支付更优惠</view>
							</view>
							<view class="delete">
								<uni-icon size="24" type="circle" color="#999"></uni-icon>
							</view>
						</view>
					</view>
					<view class="btn">立即支付 ￥118.00</view>
				</view>
			</uni-popup>
		</view>
	</view>
</template>

<script>
	import uniIcon from '../../components/uni-icon.vue';
	import uniPopup from '../../components/custom-popup.vue';
	export default {
		data() {
			return {
				showPopupPost:false,
				showPopupPayment:false,
			};
		},
		methods: {
			onPostPopup:function(){
				this.showPopupPost=true;
			},
			onPaymentPopup:function(){
				this.showPopupPayment=true;
			},
			//统一的关闭popup方法
			hidePopup: function() {
				this.showPopupPost = false;
				this.showPopupPayment = false;
			},
		},
		components: {
			uniIcon,
			uniPopup
		},
	}
</script>

<style lang="scss">
	.type {
		height: 90upx;
		padding: 0 30upx;
		background: #fff;

		.type_left {
			float: left;
			font-size: 28upx;
			line-height: 28upx;
			margin-top: 31upx;
		}

		.type_middle {
			float: right;
			font-size: 28upx;
			line-height: 28upx;
			margin-top: 31upx;
			color: rgb(102, 102, 102);
		}

		.type_right {
			float: right;
			margin-top: 30upx;
			width: 16upx;
			height: 27upx;
			vertical-align: bottom;
			margin-left: 14upx;
		}
	}

	.post {
		.van-cell {
			font-size: 30rpx;
			line-height: 30rpx;
			padding: 30rpx 32rpx;
			color: rgb(51, 51, 51);
		}
	}

	.goods {
		overflow: hidden;
		height: 260rpx;
		background: #fff;
		border-top: 1rpx solid #f2f2f2;

		.goods_left {
			float: left;
			margin: 40rpx 10rpx 40rpx 82rpx;
			.goods_img {
				width: 180rpx;
				height: 180rpx;
				background: #8E8E93;
			}
		}

		.goods_right {
			position: relative;
			float: left;
			
			.right_title {
				width: 426rpx;
				margin-top: 26rpx;
				font-size: 26rpx;
				line-height: 26rpx;
				color: #333;
			}

			.right_des {
				width: 426rpx;
				margin-top: 20rpx;
				font-size: 24rpx;
				line-height: 24rpx;
				color: #999;
			}

			.right_res {
				width: 426rpx;
				margin-top: 40rpx;
				font-size: 24rpx;
				line-height: 24rpx;
				color: #282828;
			}

			.right_price {
				width: 426rpx;
				margin-top: 26rpx;
				font-size: 26rpx;
				line-height: 26rpx;
				color: #FF000D;
			}

			.right_count {
				.stepper {
					position: absolute;
					top: 144rpx;
					right: 32rpx;
					overflow: hidden;
					margin-top: 10rpx;
					width: 50%;
					margin-left: 70rpx;

					.add,
					.subtract {
						float: left;
						width: 64rpx;
						height: 60upx;
						line-height: 60upx;
						text-align: center;
						font-size: 30rpx;
						border: 1px solid #ccc;
						box-sizing: border-box;
						color: #333;
					}

					.count {
						float: left;
						width: 60upx;
						height: 60upx;
						line-height: 60upx;
						border-top: 1px solid #ccc;
						border-bottom: 1px solid #ccc;
						text-align: center;
						box-sizing: border-box;
						min-height: 1rem;
						font-size: 26rpx;
					}

					.disabled {
						float: left;
						color: #eee;
					}
				}
			}
		}
	}

	.address {
		background: #fff;
		width: 750rpx;
		height: 140rpx;
		font-size: 28rpx;
		text-align: center;
		color: rgb(51, 51, 51);
		border-top: 1rpx solid #f2f2f2;

		.img {
			margin-top: 24upx;
			margin-bottom: 10upx;
		}

		.txt {
			height: 28upx;
			line-height: 28upx;
		}
	}
	
	.message {
		height:140upx;
		padding-top:30upx;
		padding-left:30upx;
		background: #fff;
		overflow: hidden;
		border-bottom: 1upx solid #f2f2f2;
		margin-top:15upx;
		.message_left {
			float: left;
			font-size: 28upx;
			line-height: 28upx;
		}
	
		.message_middle {
			float: left;
			width: 500upx;
			height: 110upx;
			font-size: 28upx;
			line-height: 28upx;
			color: rgb(102, 102, 102);
			.middle_txt{
				width: 500upx;
				height: 110upx;
				font-size: 28upx;
				line-height: 28upx;
				padding-left: 30upx;
			}
		}
	
		.message_right {
			float: left;
			width: 36upx;
			height: 36upx;
			margin-left: 20upx;
		}
	}
	
	.discount{
		height: 90upx;
		padding:0 30upx;
		background: #fff;
		.discount_right{
			float: left;
			font-size: 24upx;
			line-height: 24upx;
			margin-top:33upx;
			margin-left:20upx;
		}
		.discount_left{
			float: left;
			font-size: 28upx;
			line-height: 28upx;
			margin-top: 31upx;
		}
	}
	.money {
		margin-top: 20rpx;

		.item {
			overflow: hidden;
			padding: 30rpx 32rpx;
			background: #fff;
			border-bottom: 1rpx solid #f2f2f2;

			.item_left {
				float: left;
				font-size: 30rpx;
				line-height: 30rpx;
				color: rgb(51, 51, 51);
			}

			.item_right {
				float: right;
				font-size: 30rpx;
				line-height: 30rpx;
				color: rgb(51, 51, 51);
			}
		}

		.total {
			overflow: hidden;
			padding: 30rpx 32rpx;
			background: #fff;
			font-size: 30rpx;
			line-height: 30rpx;
			color: rgb(51, 51, 51);

			.total_count {
				float: right;

				.num {
					color: #FF000D;
				}
			}

			.total_right {
				float: right;

				.num {
					color: #FF000D;
				}
			}
		}
	}

	.bottom {
		position: fixed;
		bottom: 0;
		overflow: hidden;

		.bottom_left {
			float: left;
			width: 320rpx;
			padding-left: 55rpx;
			height: 100rpx;
			line-height: 100rpx;
			background: #fff;
			font-size: 24rpx;

			.num {
				color: #FF000D;
			}
		}

		.bottom_right {
			float: left;
			width: 375rpx;
			height: 100rpx;
			font-size: 24rpx;
			line-height: 100rpx;
			background: #D41C1C;
			color: #fff;
			text-align: center;
		}
	}
	
	.post{
		.post_content{
			background: #fff;
			padding-bottom:585upx;
			.content_title{
				padding-top:48upx;
				padding-bottom:44upx;
				overflow: hidden;
				position: relative;
				border-bottom: 1upx solid #f2f2f2;
				.title{
					font-size: 30upx;
					line-height: 30upx;
					color: #000;
					text-align: center;
				}
				.clear{
					position: absolute;
					top:10upx;
					right:14upx;
				}
			}
		}
		.content_item{
			padding-left: 30upx;
			padding-right: 39upx;
			height: 121upx;
			overflow: hidden;
			border-bottom: 1upx solid #f2f2f2;
			.item_title{
				float: left;
				font-size: 30upx;
				line-height: 30upx;
				margin-top:45upx;
				color: rgb(40,40,40);
			}
			.delete{
				float: right;
				margin-top:28upx;
			}
		}
	}
	.pay{
		.post_content{
			background: #fff;
			padding-bottom:130upx;
			.content_title{
				padding-top:48upx;
				padding-bottom:44upx;
				overflow: hidden;
				position: relative;
				border-bottom: 1upx solid #f2f2f2;
				.title{
					font-size: 30upx;
					line-height: 30upx;
					color: #000;
					text-align: center;
				}
				.clear{
					position: absolute;
					top:32upx;
					right:14upx;
				}
			}
		}
		.content_content{
			padding:25upx 38upx 25upx 48upx;
			.content_item{
				height: 96upx;
				overflow: hidden;
				padding:25upx 0;
				.item_left{
					float: left;
					width: 96upx;
					height: 96upx;
					border-radius: 10upx;
					background: #999;
				}
				.item_middle{
					float: left;
					width: 320upx;
					margin-left:40upx;
					.middle_title{
						font-size: 30upx;
						line-height: 30upx;
						color: rgb(40,40,40);
						margin-top:16upx;
					}
					.middle_des{
						font-size: 22upx;
						line-height: 22upx;
						color: rgb(102,102,102);
						margin-top:15upx;
					}
				}
				.delete{
					float: right;
					margin-top:18upx;
				}
			}
		}
		.btn{
			width: 690upx;
			height: 92upx;
			background: #FFD944;
			border-radius: 10upx;
			margin: 0 auto;
			line-height: 92upx;
			text-align: center;
		}
	}
</style>
