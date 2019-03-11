<template>
	<view>
		<view class="top">
			<view class="title">卖家已发货</view>
			<view class="des">查看物流信息</view>
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
		<view class="gtotal">
			<view class="item">
				<view class="item_left">商品总价</view>
				<view class="item_right">¥20999</view>
			</view>
		</view>
		<view class="post">
			<view class="item">
				<view class="item_left">运费（快递）</view>
				<view class="item_right">¥0.00</view>
			</view>
		</view>
		<view class="post">
			<view class="item">
				<view class="item_left">运费险（卖家赠送）</view>
				<view class="item_right">¥0.00</view>
			</view>
		</view>
		<view class="dtotal">
			<view class="item">
				<view class="item_left">订单总价</view>
				<view class="item_right">¥20999</view>
			</view>
		</view>
		<view class="acture">
			<view class="item">
				<view class="item_left">实付款</view>
				<view class="item_right">¥20999</view>
			</view>
		</view>
		<view class="dinfo">
			<view class="item">
				<view class="item_left">订单信息</view>
				<view class="item_right">¥20999</view>
			</view>
		</view>
		<view class="infol">
			<view class="item">
				<view class="item_left">订单编号:</view>
				<view class="item_right">365870465400445475</view>
			</view>
		</view>
		<view class="infol">
			<view class="item">
				<view class="item_left">支付宝交易号:</view>
				<view class="item_right">201903042201118451028772588</view>
			</view>
		</view>
		<view class="infol">
			<view class="item">
				<view class="item_left">创建时间:</view>
				<view class="item_right">2019-03-04 13:20:59</view>
			</view>
		</view>
		<view class="infol">
			<view class="item">
				<view class="item_left">付款时间:</view>
				<view class="item_right">2019-03-04 13:20:59</view>
			</view>
		</view>
		<view class="infol">
			<view class="item">
				<view class="item_left">发货时间:</view>
				<view class="item_right">2019-03-04 13:20:59</view>
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
	.top {
		background: #fff;
		padding-top: 62upx;
		padding-bottom: 42upx;
		padding-left: 60upx;

		.title {
			font-size: 36upx;
			line-height: 36upx;
			color: rgb(34, 34, 34);
		}

		.des {
			margin-top: 38upx;
			font-size: 28upx;
			line-height: 28upx;
			color: rgb(255, 158, 118);

			text {
				color: red;
			}
		}
	}

	.address {
		overflow: hidden;
		height: 156upx;
		background: #fff;
		border-top: 1upx solid #f2f2f2;

		.address_left {
			float: left;

			.left_icon {
				width: 28upx;
				height: 36upx;
				margin-top: 68upx;
				margin-left: 30upx;
			}

		}

		.address_right {
			float: left;
			margin-left: 36upx;
			width: 596upx;

			.right_title {
				font-size: 28upx;
				line-height: 28upx;
				margin-top: 26upx;
			}

			.right_des {
				font-size: 28upx;
				line-height: 34upx;
				margin-top: 12upx;
			}
		}
	}

	.goods {
		background: #fff;
		padding: 12upx 43upx;
		overflow: hidden;
		margin-top: 15upx;

		.goods_left {
			float: left;
			width: 140upx;
			height: 140upx;
			border-radius: 10upx;
			background: red;
		}

		.goods_right {
			float: left;
			margin-left: 24upx;

			.right_title {
				font-size: 30upx;
				line-height: 30upx;
				margin-top: 40upx;
				color: rgb(40, 40, 40);
			}

			.right_des {
				line-height: 24upx;
				overflow: hidden;
				margin-top: 20upx;

				.des_num {
					float: left;
					font_size: 24upx;
					line-height: 24upx;
					color: rgb(101, 101, 101)
				}

				.des_total {
					float: right;
					font_size: 24upx;
					line-height: 24upx;
					color: rgb(101, 101, 101);

					text {
						color: red;
						margin-left: 10upx;
					}
				}
			}
		}
	}

	.gtotal{
		margin-top: 16upx;
		.item {
			padding:57upx 57upx 16upx 32upx;
			background: #fff;
			overflow: hidden;
			.item_left{
				float: left;
				font-size:28upx;
				line-height:28upx;
				color: rgb(102,102,102);
			}
			.item_right{
				float: right;
				font-size:28upx;
				line-height:28upx;
				color: rgb(102,102,102);
			}
		}
	}
	.post{
		.item {
			padding:16upx 57upx 16upx 32upx;
			background: #fff;
			overflow: hidden;
			.item_left{
				float: left;
				font-size:28upx;
				line-height:28upx;
				color: rgb(102,102,102);
			}
			.item_right{
				float: right;
				font-size:28upx;
				line-height:28upx;
				color: rgb(102,102,102);
			}
		}
	}
	.dtotal{
		.item {
			padding:18upx 57upx 38upx 32upx;
			background: #fff;
			overflow: hidden;
			.item_left{
				float: left;
				font-size:32upx;
				line-height:32upx;
				color: rgb(40,40,40);
			}
			.item_right{
				float: right;
				font-size:32upx;
				line-height:32upx;
				color: rgb(40,40,40);
			}
		}
	}
	.acture{
		border-top: 2upx solid #f2f2f2;
		.item {
			padding:30upx 57upx 30upx 32upx;
			background: #fff;
			overflow: hidden;
			.item_left{
				float: left;
				font-size:32upx;
				line-height:32upx;
				color: rgb(40,40,40);
			}
			.item_right{
				float: right;
				font-size:32upx;
				line-height:32upx;
				color: rgb(255,146,101);
			}
		}
	}
	.dinfo{
		border-bottom: 2upx solid #f2f2f2;
		margin-top:15upx;
		.item {
			padding:30upx 57upx 30upx 32upx;
			background: #fff;
			overflow: hidden;
			.item_left{
				float: left;
				font-size:32upx;
				line-height:32upx;
				color: rgb(40,40,40);
			}
			.item_right{
				float: right;
				font-size:32upx;
				line-height:32upx;
				color: rgb(255,146,101);
			}
		}
	}
	.infol{
		.item {
			padding:18upx 57upx 18upx 32upx;
			background: #fff;
			overflow: hidden;
			.item_left{
				float: left;
				font-size:28upx;
				line-height:28upx;
				color: rgb(102,102,102);
			}
			.item_right{
				float: right;
				font-size:28upx;
				line-height:28upx;
				color: rgb(102,102,102);
			}
		}
	}
</style>
