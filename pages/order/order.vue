<template>
	<view>
		<view style="background: #fff;">
			<uni-segmented-control :current="current" :values="items" styleType="text" v-on:clickItem="onClickItem">
			</uni-segmented-control>
		</view>
		<view class="content">
			<view v-show="current === 0">
				<view class="null">
					<image class="null_img" src="/static/empty.png"></image>
					<view class="null_txt">暂无订单</view>
				</view>
			</view>
			<view v-show="current === 1">
				<view class="content">
					<view class="item">
						<view class="header">
							<view class="header_left">2019-01-21 10:45</view>
							<view class="header_right">已完成</view>
						</view>
						<view class="center">
							<view class="center_left">
								<image class="left_img" src=""></image>
							</view>
							<view class="center_middle">
								<view class="middle_title">BEELY彼丽四味足汤 足浴包 泡脚药包 一盒10袋 共40袋</view>
								<view class="middle_des">规格：一盒10袋（共40袋）</view>
								<view class="middle_post">包邮</view>
							</view>
							<view class="center_right">
								<view class="right_price">￥99.00</view>
								<view class="right_num">x1</view>
							</view>
						</view>
						<view class="bottom">
							<view class="bottom_top">
								应付款：<text class="price">￥99.00</text>（含运费：￥0.00）
							</view>
							<view class="bottom_btn">
								<view class="btn circle">删除</view>
								<view class="btn entry">再次购买</view>
							</view>
						</view>
					</view>
					<view class="item margin24">
						<view class="header">
							<view class="header_left">2019-01-21 10:45</view>
							<view class="header_right">已完成</view>
						</view>
						<view class="center">
							<view class="center_left">
								<image class="left_img" src=""></image>
							</view>
							<view class="center_middle">
								<view class="middle_title">BEELY彼丽四味足汤 足浴包 泡脚药包 一盒10袋 共40袋</view>
								<view class="middle_des">规格：一盒10袋（共40袋）</view>
								<view class="middle_post">包邮</view>
							</view>
							<view class="center_right">
								<view class="right_price">￥99.00</view>
								<view class="right_num">x1</view>
							</view>
						</view>
						<view class="bottom">
							<view class="bottom_top">
								应付款：<text class="price">￥99.00</text>（含运费：￥0.00）
							</view>
							<view class="bottom_btn">
								<view class="btn circle">删除</view>
								<view class="btn entry">再次购买</view>
							</view>
						</view>
					</view>
					<view class="empty">没有更多了~</view>
				</view>
			</view>
			<view v-show="current === 2">
				<view class="content">
					<view class="item">
						<view class="header">
							<view class="header_left">2019-01-21 10:45</view>
							<view class="header_right">已完成</view>
						</view>
						<view class="center">
							<view class="center_left">
								<image class="left_img" src=""></image>
							</view>
							<view class="center_middle">
								<view class="middle_title">BEELY彼丽四味足汤 足浴包 泡脚药包 一盒10袋 共40袋</view>
								<view class="middle_des">规格：一盒10袋（共40袋）</view>
								<view class="middle_post">包邮</view>
							</view>
							<view class="center_right">
								<view class="right_price">￥99.00</view>
								<view class="right_num">x1</view>
							</view>
						</view>
						<view class="bottom">
							<view class="bottom_top">
								应付款：<text class="price">￥99.00</text>（含运费：￥0.00）
							</view>
							<view class="bottom_btn">
								<view class="btn circle">删除</view>
								<view class="btn entry">再次购买</view>
							</view>
						</view>
					</view>
					<view class="item margin24">
						<view class="header">
							<view class="header_left">2019-01-21 10:45</view>
							<view class="header_right">已完成</view>
						</view>
						<view class="center">
							<view class="center_left">
								<image class="left_img" src=""></image>
							</view>
							<view class="center_middle">
								<view class="middle_title">BEELY彼丽四味足汤 足浴包 泡脚药包 一盒10袋 共40袋</view>
								<view class="middle_des">规格：一盒10袋（共40袋）</view>
								<view class="middle_post">包邮</view>
							</view>
							<view class="center_right">
								<view class="right_price">￥99.00</view>
								<view class="right_num">x1</view>
							</view>
						</view>
						<view class="bottom">
							<view class="bottom_top">
								应付款：<text class="price">￥99.00</text>（含运费：￥0.00）
							</view>
							<view class="bottom_btn">
								<view class="btn circle">删除</view>
								<view class="btn entry">再次购买</view>
							</view>
						</view>
					</view>
					<view class="empty">没有更多了~</view>
				</view>
			</view>
			<view v-show="current === 3">
				<view class="content">
					<view class="item">
						<view class="header">
							<view class="header_left">2019-01-21 10:45</view>
							<view class="header_right">已完成</view>
						</view>
						<view class="center">
							<view class="center_left">
								<image class="left_img" src=""></image>
							</view>
							<view class="center_middle">
								<view class="middle_title">BEELY彼丽四味足汤 足浴包 泡脚药包 一盒10袋 共40袋</view>
								<view class="middle_des">规格：一盒10袋（共40袋）</view>
								<view class="middle_post">包邮</view>
							</view>
							<view class="center_right">
								<view class="right_price">￥99.00</view>
								<view class="right_num">x1</view>
							</view>
						</view>
						<view class="bottom">
							<view class="bottom_top">
								应付款：<text class="price">￥99.00</text>（含运费：￥0.00）
							</view>
							<view class="bottom_btn">
								<view class="btn circle">删除</view>
								<view class="btn entry">再次购买</view>
							</view>
						</view>
					</view>
					<view class="item margin24">
						<view class="header">
							<view class="header_left">2019-01-21 10:45</view>
							<view class="header_right">已完成</view>
						</view>
						<view class="center">
							<view class="center_left">
								<image class="left_img" src=""></image>
							</view>
							<view class="center_middle">
								<view class="middle_title">BEELY彼丽四味足汤 足浴包 泡脚药包 一盒10袋 共40袋</view>
								<view class="middle_des">规格：一盒10袋（共40袋）</view>
								<view class="middle_post">包邮</view>
							</view>
							<view class="center_right">
								<view class="right_price">￥99.00</view>
								<view class="right_num">x1</view>
							</view>
						</view>
						<view class="bottom">
							<view class="bottom_top">
								应付款：<text class="price">￥99.00</text>（含运费：￥0.00）
							</view>
							<view class="bottom_btn">
								<view class="btn circle">删除</view>
								<view class="btn entry">再次购买</view>
							</view>
						</view>
					</view>
					<view class="empty">没有更多了~</view>
				</view>
			</view>
			<view v-show="current === 4">
				<view class="content">
					<view class="item">
						<view class="header">
							<view class="header_left">2019-01-21 10:45</view>
							<view class="header_right">已完成</view>
						</view>
						<view class="center">
							<view class="center_left">
								<image class="left_img" src=""></image>
							</view>
							<view class="center_middle">
								<view class="middle_title">BEELY彼丽四味足汤 足浴包 泡脚药包 一盒10袋 共40袋</view>
								<view class="middle_des">规格：一盒10袋（共40袋）</view>
								<view class="middle_post">包邮</view>
							</view>
							<view class="center_right">
								<view class="right_price">￥99.00</view>
								<view class="right_num">x1</view>
							</view>
						</view>
						<view class="bottom">
							<view class="bottom_top">
								应付款：<text class="price">￥99.00</text>（含运费：￥0.00）
							</view>
							<view class="bottom_btn">
								<view class="btn circle">删除</view>
								<view class="btn entry">再次购买</view>
							</view>
						</view>
					</view>
					<view class="item margin24">
						<view class="header">
							<view class="header_left">2019-01-21 10:45</view>
							<view class="header_right">已完成</view>
						</view>
						<view class="center">
							<view class="center_left">
								<image class="left_img" src=""></image>
							</view>
							<view class="center_middle">
								<view class="middle_title">BEELY彼丽四味足汤 足浴包 泡脚药包 一盒10袋 共40袋</view>
								<view class="middle_des">规格：一盒10袋（共40袋）</view>
								<view class="middle_post">包邮</view>
							</view>
							<view class="center_right">
								<view class="right_price">￥99.00</view>
								<view class="right_num">x1</view>
							</view>
						</view>
						<view class="bottom">
							<view class="bottom_top">
								应付款：<text class="price">￥99.00</text>（含运费：￥0.00）
							</view>
							<view class="bottom_btn">
								<view class="btn circle">删除</view>
								<view class="btn entry">再次购买</view>
							</view>
						</view>
					</view>
					<view class="empty">没有更多了~</view>
				</view>
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
					'全部',
					'待付款',
					'待发货',
					'待收获',
					'待评价'
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
	.content {
		.item {
			.header {
				overflow: hidden;
				padding: 24upx 34upx 24upx 34upx;
				background: #fff;

				.header_left {
					float: left;
					font-size: 21upx;
					line-height: 21upx;
					color: #666666;
				}

				.header_right {
					float: right;
					font-size: 21upx;
					line-height: 21upx;
					color: #3E3E3E;
				}
			}

			.center {
				overflow: hidden;
				padding: 12upx 34upx 20upx 20upx;
				background: #fff;
				border-bottom: 1upx solid #F2F2F2;

				.center_left {
					float: left;

					.left_img {
						width: 152upx;
						height: 152upx;
						background: #3E3E3E;
						vertical-align: bottom;
					}
				}

				.center_middle {
					float: left;
					margin-left: 20upx;
					width: 330upx;

					.middle_title {
						height: 60upx;
						font-size: 24upx;
						line-height: 30upx;
						color: rgb(51, 51, 51);
					}

					.middle_des {
						margin-top: 22upx;
						font-size: 24upx;
						line-height: 24upx;
						color: rgb(153, 153, 153);
					}

					.middle_post {
						font-size: 18upx;
						color: #fff;
						width: 50upx;
						height: 26upx;
						line-height: 26upx;
						text-align: center;
						background: #FFD944;
						border-radius: 6upx;
						margin-top: 22upx;
					}
				}

				.center_right {
					float: right;

					.right_price {
						font-size: 24upx;
						line-height: 24upx;
						color: rgb(51, 51, 51);
					}

					.right_num {
						margin-top: 20upx;
						text-align: right;
						font-size: 24upx;
						line-height: 24upx;
						color: rgb(153, 153, 153);
					}
				}
			}

			.bottom {
				padding: 36upx 20upx 24upx 0;
				background: #fff;

				.bottom_top {
					text-align: right;
					font-size: 24upx;
					color: rgb(153, 153, 153);
					line-height: 25upx;

					.price {
						font-size: 25upx;
						color: rgb(51, 51, 51);
					}
				}

				.bottom_btn {
					overflow: hidden;
					margin-top: 28upx;

					.btn {
						float: right;
						width: 152upx;
						height: 54upx;
						margin-right: 20upx;
						font-size: 26upx;
						line-height: 54upx;
						text-align: center;
						color: #424242;
						border: 1upx solid #929292;
						border-radius: 4upx;
					}

					.entry {
						border-color: #FFD944;
						background: #FFD944;
					}

				}
			}
		}

		.margin24 {
			margin-top: 24upx;
		}

		.empty {

			margin-top: 42upx;
			text-align: center;
			font-size: 24upx;
			color: rgb(153, 153, 153);
		}
	}

	.null {
		.null_img {
			width: 632upx;
			height: 464upx;
			margin-left: 59upx;
			margin-top: 242upx;
		}

		.null_txt {
			font-size: 24upx;
			line-height: 24upx;
			text-align: center;
			color: rgb(153, 153, 153);
		}
	}
</style>
