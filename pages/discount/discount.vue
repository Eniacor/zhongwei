<template>
	<view>
		<view class="header">
			<uni-segmented-control :current="current" :values="items" v-on:clickItem="onClickItem">
			</uni-segmented-control>
		</view>
		<view class="content">
			<view v-show="current === 0">
				<view class="null">
					<image class="null_img" src="/static/empty.png"></image>
				</view>
			</view>
			<view v-show="current === 1">
				<view class="content">
					<view class="item">
						<view class="item_left">
							<image class="left_img"></image>
							<view class="left_right">
								<view class="right_title">软壳vivo苹果oppp手机壳</view>
								<view class="right_des">单价 ￥6.9</view>
								<view class="right_discount">
									<text class="txt">领券后 ￥</text>
									<text class="price">6.9</text>
								</view>
							</view>
						</view>
						<view class="item_middle"></view>
						<view class="item_right">
							<view class="right_price">
								<text class="price_dot">￥</text>
								<text class="price_num">2</text>
							</view>
							<view class="right_des">无门槛券</view>
							<view class="right_btn">立即使用</view>
							<view class="right_intro">仅剩2天</view>
						</view>
					</view>
					<view class="item">
						<view class="item_left">
							<image class="left_img"></image>
							<view class="left_right">
								<view class="right_title">软壳vivo苹果oppp手机壳</view>
								<view class="right_des">单价 ￥6.9</view>
								<view class="right_discount">
									<text class="txt">领券后 ￥</text>
									<text class="price">6.9</text>
								</view>
							</view>
						</view>
						<view class="item_middle"></view>
						<view class="item_right">
							<view class="right_price">
								<text class="price_dot">￥</text>
								<text class="price_num">2</text>
							</view>
							<view class="right_des">无门槛券</view>
							<view class="right_btn get">已使用</view>
						</view>
					</view>
					<view class="item">
						<view class="item_left">
							<image class="left_img"></image>
							<view class="left_right">
								<view class="right_title">软壳vivo苹果oppp手机壳</view>
								<view class="right_des">单价 ￥6.9</view>
								<view class="right_discount">
									<text class="txt">领券后 ￥</text>
									<text class="price">6.9</text>
								</view>
							</view>
						</view>
						<view class="item_middle"></view>
						<view class="item_right">
							<view class="right_price">
								<text class="price_dot">￥</text>
								<text class="price_num">2</text>
							</view>
							<view class="right_des">无门槛券</view>
							<view class="right_btn used">已失效</view>
						</view>
					</view>
				</view>
			</view>
			<view v-show="current === 2">

			</view>
		</view>
	</view>
</template>

<script>
	import uniSegmentedControl from '../../components/uni-segmented-order.vue';
	export default {
		data() {
			return {
				items: [
					'未使用（4）',
					'已使用（4）',
					'已失效（7）',
				],
				current: 0,
			};
		},
		components: {
			uniSegmentedControl,
		},
		methods: {
			onClickItem(index) {
				if (this.current !== index) {
					this.current = index;
				}
			},
		}
	}
</script>

<style lang="scss">
	.header {
		background: #fff;
	}

	.content {
		.item {
			overflow: hidden;
			margin: 16upx 24upx;
			position: relative;

			.item_left {
				float: left;
				width: 458upx;
				border-radius: 16upx;
				background: #fff;
				padding: 37upx 27upx;

				.left_img {
					float: left;
					width: 200upx;
					height: 200upx;
					vertical-align: bottom;
					background: #F2F2F2;
				}

				.left_right {
					float: left;
					margin-left: 21upx;

					.right_title {
						width: 220upx;
						margin-top: 16upx;
						font-size: 26upx;
						line-height: 44upx;
						height: 78upx;
					}

					.right_des {
						margin-top: 35upx;
						font-size: 24upx;
						line-height: 24upx;
						color: rgb(153, 153, 153);
					}

					.right_discount {
						.txt {
							font-size: 24upx;
							color: #DB4040;
						}

						.price {
							font-size: 30upx;
							color: #D41C1C;
						}
					}
				}
			}

			.item_middle {
				position: absolute;
				top: 16upx;
				left: 507upx;
				width: 2upx;
				height: 240upx;
				border-right: 4upx dotted #cac6c6;
			}

			.item_right {
				float: left;
				width: 190upx;
				background: #fff;
				border-radius: 16upx;
				padding-top:36upx;
				padding-bottom: 33upx;

				.right_price {
					text-align: center;
					.price_dot {
						font-size: 20upx;
						line-height: 44upx;
						color: #D41C1C;
					}

					.price_num {
						font-size: 44upx;
						line-height: 44upx;
						color: #D72B2B;
					}
				}

				.right_des {
					margin-top: 18upx;
					font-size: 26upx;
					line-height: 26upx;
					color: #D41C1C;
					text-align: center;
				}

				.right_btn {
					width: 126upx;
					height: 64upx;
					text-align: center;
					line-height: 64upx;
					font-size: 24upx;
					color: rgb(51, 51, 51);
					background: #FFD944;
					border-radius: 10upx;
					margin: 0 auto;
					margin-top: 16upx;
					margin-bottom: 11upx;
				}

				.get {
					margin-top: 40upx;
					background: #D41C1C;
					color: #fff;
				}

				.used {

					margin-top: 40upx;
					background: #FF6A6C;
					color: #fff;
				}

				.right_intro {
					font-size: 24upx;
					line-height: 24upx;
					color: #D41C1C;
					text-align: center;
				}
			}
		}

	}

	.null {
		.null_img {
			width: 632upx;
			height: 464upx;
			margin-left: 59upx;
			margin-top: 242upx;
		}
	}
</style>
