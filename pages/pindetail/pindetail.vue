<template>
	<view>
		<view>
			<uni-segmented-control :current="current" :values="items" styleType="text" v-on:clickItem="onClickItem">
			</uni-segmented-control>
		</view>
		<view class="container">
			<view v-show="current === 0">
				<view class="content">
					<swiper class="slide_swiper" :autoplay="autoplay" :interval="interval" :duration="duration">
						<swiper-item>
							<view class="info">
								<view class="collect">
									<uni-icon size="16" type="star" color="#fff"></uni-icon>
									<text class="collect_txt">收藏</text>
								</view>
								<view class="page">1/3</view>
							</view>
						</swiper-item>
						<swiper-item>
							<view class="info">
								<view class="collect">
									<uni-icon size="16" type="star" color="#fff"></uni-icon>
									<text class="collect_txt">收藏</text>
								</view>
								<view class="page">2/3</view>
							</view>
						</swiper-item>
						<swiper-item>
							<view class="info">
								<view class="collect">
									<uni-icon size="16" type="star" color="#fff"></uni-icon>
									<text class="collect_txt">收藏</text>
								</view>
								<view class="page">3/3</view>
							</view>
						</swiper-item>
					</swiper>
					<view class="des">
						<view class="price">
							<text class="ping">两人团：</text>
							<text class="current">￥118</text>
							<text class="origin">￥118</text>
							<text class="ping_time">距离结束1天21时26分36秒</text>
						</view>
						<view class="post">
							<view class="post_txt">
								满100免邮费
							</view>
						</view>
						<view class="title">网红便携式手持电熨斗</view>
					</view>
					<view class="send">
						<image class="send_img" src="/static/post_cart.png"></image>
						<text class="send_txt">48小时发货</text>
					</view>
					<view class="tuan">
						<view class="tuan_title">
							<view class="title_label">17人在拼单，可直接参与</view>
							<image class="title_icon" src="/images/static/my.png"></image>
							<view class="title_value">查看全部</view>
						</view>
						<view class="tuan_item">
							<image class="item_avatar" src=""></image>
							<view class="item_label">快乐每一天</view>
							<view class="item_btn">去拼单</view>
							<view class="item_value">
								<view class="value_top">还差1人拼成</view>
								<view class="value_bottom">剩余23:53:35</view>
							</view>
						</view>
					</view>
					<view class="address">
						<view class="address_label">地址</view>
						<view class="address_value">选择收货地址</view>
						<image class="address_icon" src="/static/my.png"></image>
					</view>
					<view class="bottom_bar">
						<detail-bar></detail-bar>
					</view>
				</view>
			</view>
			<view v-show="current === 1" style="background: #fff;">
				<view class="discuss_tab">
					<uni-button-control :current="ccurrent" :values="citems" v-on:clickItem="onClickCItem">
					</uni-button-control>
				</view>
				<view v-show="ccurrent === 0">
					<view class="discuss">
						<view class="header">
							<view class="header_label">商品评价(257)</view>
							<image class="header_icon" src="/images/static/my.png"></image>
							<view class="header_value">查看全部</view>
						</view>
						<view class="item">
							<view class="item_header">
								<image class="header_avatar"></image>
								<view class="header_txt">环球小荐人</view>
								<view class="header_time">4小时前发布</view>
							</view>
							<view class="item_des">
								普通的眼罩你肯定见过，那蒸汽眼罩你见过？
								普通的眼罩你肯定见过，那蒸汽眼罩你见过？
								普通的眼罩你肯定见过，那蒸汽眼罩你见过？
								普通的眼罩你肯定见过，那蒸汽眼罩你见过？
							</view>
							<view class="item_imgs">
								<image class="img"></image>
								<image class="img"></image>
								<image class="img"></image>
								<image class="img"></image>
								<image class="img"></image>
							</view>
							<view class="item_date">2019.01.27 颜色：蓝色 500ml</view>
						</view>
					</view>
				</view>
				<view v-show="ccurrent === 1">
					ffffff
				</view>
				<view v-show="ccurrent === 2">
					ffff
				</view>
			</view>
			<view v-show="current === 2">
				<view class="goods">
					<view class="goods_title">商品详情</view>
					<image class="goods_img"></image>
					<image class="goods_img"></image>
				</view>
			</view>
		</view>

		<view class="attr">
			<uni-popup :show="showPopupGui" type="bottom" v-on:hidePopup="hidePopup">
				<view class="popup_attr">
					<view class="back">
						<image class="img"></image>
						<view class="attr_top">
							<view class="top_right">
								<image class="right_close" src="/static/close.png" @click="hidePopup"></image>
							</view>
							<view class="top_middle">
								<view class="des_price">￥118</view>
								<view class="des_count">库存9971</view>
								<view class="des_select">已选择："150ml"</view>
							</view>
						</view>
					</view>
					<view class="attr_gui">
						<view class="gui_title">规格</view>
						<view class="gui_list">
							<view class="gui_item gactive">100ml</view>
							<view class="gui_item">150ml</view>
						</view>
					</view>
					<view class="attr_color">
						<view class="color_title">颜色分类</view>
						<view class="color_list">
							<view class="color_item cactive">
								<image class="item_img" src=""></image>
								<text class="item_txt">100ml</text>
							</view>
							<view class="color_item">
								<image class="item_img" src=""></image>
								<text class="item_txt">100ml</text>
							</view>
						</view>
					</view>
					<view class="num">
						<view class="num_left">购买数量</view>
						<view class="num_right">
							<uni-number-box></uni-number-box>
						</view>
					</view>
					<view class="bottoms">
						<view class="bottoms_cart">加入购物车</view>
						<view class="bottoms_buy">确定</view>
					</view>
				</view>
			</uni-popup>
		</view>
		<view class="pin">
			<uni-popup :show="showPopupPin" type="middle" v-on:hidePopup="hidePopup">
				<view class="popup_ping">
					<view class="ping_delete">
						<uni-icon size="34" type="closeempty" color="#696969"></uni-icon>
					</view>
					<view class="ping_title">参与xxx的拼单</view>
					<view class="ping_des">晋升1个名额，23:58:37后结束</view>
					<view class="ping_img">
						<image class="img1" src="/static/ping4.png"></image>
						<image class="img2" src="/static/ping4.png"></image>
					</view>
					<view class="ping_btn">参与拼单</view>
				</view>
			</uni-popup>
		</view>
		<view class="can">
			<uni-popup :show="showPopupCan" type="middle" v-on:hidePopup="hidePopup">
				<view class="popup_can">
					<view class="can_delete">
						<uni-icon size="34" type="closeempty" color="#696969"></uni-icon>
					</view>
					<view class="can_title">正在拼单</view>
					<view class="can_item">
						<view class="item_left">
							<image class="left_img" src="/static/ping4.png"></image>
						</view>
						<view class="item_middle">
							<view class="middle_top">
								<text class="top_name">林舒</text>
								<text class="top_num">还差1个人</text>
							</view>
							<view class="middle_bottom">
								剩余23:53:35
							</view>
						</view>
						<view class="item_right">去拼单</view>
					</view>
				</view>
			</uni-popup>
		</view>
	</view>
</template>

<script>
	import uniSegmentedControl from '../../components/uni-segmented-order.vue';
	import uniButtonControl from '../../components/uni-button-control.vue';
	import uniPopup from '../../components/uni-popup.vue';
	import detailBar from '../../components/detail-bar.vue';
	import uniNumberBox from '../../components/uni-number-box.vue'
	import uniIcon from '../../components/uni-icon.vue';
	export default {
		data() {
			return {
				items: [
					'商品',
					'评价',
					'详情',
				],
				citems: [
					'全部（1044）',
					'追加（441）',
					'有图（2357）',
					'质量很好（105344）'
				],
				current: 0,
				ccurrent: 0,
				indicatorDots: true,
				autoplay: true,
				interval: 5000,
				duration: 1000,
				showPopupGui: false,
				showPopupPin: false,
				showPopupCan: false,
			}
		},
		components: {
			uniSegmentedControl,
			uniPopup,
			uniButtonControl,
			detailBar,
			uniNumberBox,
			uniIcon
		},
		methods: {
			onClickItem(index) {
				if (this.current !== index) {
					this.current = index;
				}
			},
			onClickCItem(index) {
				if (this.ccurrent !== index) {
					this.ccurrent = index;
				}
			},
			hidePopup: function() {
				this.showPopupGui = false;
				this.showPopupPin = false;
				this.showPopupCan = false;
			},
			showGuiPopup: function() {
				this.hidePopup();
				this.showPopupGui = true;
			},
			showPinPopup: function() {
				this.hidePopup();
				this.showPopupPin = true;
			},
			showCanPopup: function() {
				this.hidePopup();
				this.showPopupCan = true;
			},
		}
	}
</script>

<style lang="scss">
	page {
		height: auto;
		background-color: #f7f7f7;
		margin-bottom: 100upx;
	}

	.container {
		.content {
			.slide_swiper {
				width: 750upx;
				height: 734upx;

				 .info{
					text-align: right;
					margin-top: 650upx;
					vertical-align: middle;
					.collect{
						display: inline;
						margin-right: 20upx;
						border-radius: 30upx;
						padding:10upx 16upx;
						background: rgba($color: #000000, $alpha: .3);
						.collect_txt{
							font-size: 24upx;
							line-height: 24upx;
							color: #fff;
						}
					}
					.page{
						display: inline;
						margin-right: 50upx;
						border-radius: 30upx;
						padding:12upx 30upx;
						background: rgba($color: #000000, $alpha: .3);
						font-size: 24upx;
						line-height: 24upx;
						color: #fff;
					}
				}
			}

			.des {
				padding: 40rpx 22rpx 30rpx 22rpx;
				background: #fff;

				.price {
					font-size: 30rpx;
					line-height: 30rpx;

					.current {
						color: rgb(255, 0, 13);
					}

					.origin {
						text-decoration: line-through;
						color: rgb(152, 152, 152);
						margin-left: 12rpx;
					}
				}

				.post {
					display: inline-block;
					margin: 0;
					padding: 0;
					margin-top: 36rpx;
					border: 2rpx solid rgb(255, 0, 13);
					border-radius: 4rpx;
					color: rgb(255, 0, 13);
					line-height: 18upx;
					.post_txt {
						display: inline-block;
						font-size: 20rpx;
					}

				}

				.title {
					font-size: 36rpx;
					line-height: 36rpx;
					margin-top: 26rpx;
					color: rgb(40, 40, 40);
				}
			}

			.send {
				overflow: hidden;
				padding: 30upx 22upx;
				background: #fff;
				border-top: 1upx solid #f2f2f2;
				border-bottom: 1upx solid #f2f2f2;

				.send_img {
					float: left;
					width: 34upx;
					height: 34upx;
					border-radius: 50%;
				}

				.send_txt {
					float: left;
					font-size: 30upx;
					line-height: 30upx;
					color: rgb(152, 152, 152);
					margin-left: 20upx;
					margin-top: 4upx;
				}
			}

			.shop {
				overflow: hidden;
				background: #fff;
				padding: 35upx 22upx;
				margin-bottom: 16upx;

				.shop_label {
					float: left;
					width: 58upx;
					height: 58upx;
					border-radius: 50%;
					background: #333;
				}

				.shop_value {
					float: left;
					font-size: 30upx;
					line-height: 30upx;
					color: rgb(51, 51, 51);
					margin-left: 25upx;
					margin-top: 18upx;
				}

				.shop_icon {
					float: right;
					width: 16upx;
					height: 27upx;
					margin-left: 20upx;
					margin-top: 18upx;
				}
			}

			.tuan {
				margin-top: 16rpx;

				.tuan_title {
					overflow: hidden;
					background: #fff;
					padding: 30rpx 22rpx;
					border-bottom: 1rpx solid #f2f2f2;

					.title_label {
						float: left;
						font-size: 30rpx;
						line-height: 30rpx;
						color: #333;
					}

					.title_value {
						float: right;
						font-size: 30rpx;
						line-height: 30rpx;
						color: #999;
						margin-left: 45rpx;
					}

					.title_icon {
						float: right;
						width: 16rpx;
						height: 27rpx;
						margin-left: 20rpx;
					}
				}

				.tuan_item {
					background: #fff;
					overflow: hidden;
					border-bottom: 1rpx solid #f2f2f2;

					.item_avatar {
						float: left;
						margin-top: 25rpx;
						margin-left: 22rpx;
						margin-bottom: 23rpx;
						width: 74rpx;
						height: 74rpx;
						border-radius: 50%;
						background: #333;
					}

					.item_label {
						float: left;
						font-size: 30rpx;
						line-height: 30rpx;
						color: #333;
						margin-top: 45rpx;
						margin-left: 16rpx;

					}

					.item_btn {
						float: right;
						margin-right: 26rpx;
						margin-left: 22rpx;
						margin-top: 30rpx;
						width: 138rpx;
						height: 62rpx;
						border-radius: 6rpx;
						font-size: 24rpx;
						line-height: 62rpx;
						text-align: center;
						background: #D41C1C;
						color: #fff;
					}

					.item_value {
						float: right;

						.value_top {
							margin-top: 26rpx;
							font-size: 26rpx;
							line-height: 26rpx;
							color: #333;
						}

						.value_bottom {
							margin-top: 10rpx;
							font-size: 26rpx;
							line-height: 26rpx;
							color: #999;
						}
					}
				}
			}

			.gui {
				overflow: hidden;
				background: #fff;
				padding: 30upx 22upx;
				border-bottom: 1upx solid #f2f2f2;

				.gui_label {
					float: left;
					font-size: 30upx;
					line-height: 30upx;
					color: #666;
				}

				.gui_value {
					float: left;
					font-size: 30upx;
					line-height: 30upx;
					color: rgb(51, 51, 51);
					margin-left: 45upx;
				}

				.gui_icon {
					float: right;
					width: 16upx;
					height: 27upx;
					margin-left: 20upx;
				}
			}

			.address {
				overflow: hidden;
				background: #fff;
				padding: 30upx 22upx;
				margin-bottom: 16upx;

				.address_label {
					float: left;
					font-size: 30upx;
					line-height: 30upx;
					color: #666;
				}

				.address_value {
					float: left;
					font-size: 30upx;
					line-height: 30upx;
					color: rgb(51, 51, 51);
					margin-left: 45upx;
				}

				.address_icon {
					float: right;
					width: 16upx;
					height: 27upx;
					margin-left: 20upx;
				}
			}

			.discuss {
				.header {
					overflow: hidden;
					background: #fff;
					padding: 30upx 22upx;

					.header_label {
						float: left;
						font-size: 30upx;
						line-height: 30upx;
						color: rgb(40, 40, 40);
					}

					.header_value {
						float: right;
						font-size: 30upx;
						line-height: 30upx;
						color: rgb(102, 102, 102);
					}

					.header_icon {
						float: right;
						width: 16upx;
						height: 27upx;
						margin-left: 20upx;
					}
				}

				.item {
					.item_header {
						margin-top: 16upx;
						overflow: hidden;
						height: 80upx;
						background: #fff;

						.header_avatar {
							float: left;
							width: 58upx;
							height: 58upx;
							background: #333;
							border-radius: 50%;
							margin-left: 26upx;
							margin-top: 22upx;
						}

						.header_txt {
							float: left;
							font-size: 30upx;
							line-height: 30upx;
							color: rgb(51, 51, 51);
							margin-top: 40upx;
							margin-left: 20upx;
						}

						.header_time {
							float: left;
							font-size: 24upx;
							line-height: 24upx;
							color: rgb(102, 102, 102);
							margin-top: 42upx;
							margin-left: 30upx;
						}
					}

					.item_des {
						font-size: 30upx;
						line-height: 46upx;
						color: rgb(51, 51, 51);
						padding: 16upx 26upx;
						background: #fff;
					}

					.item_imgs {
						padding: 0 11upx 0 19upx;
						overflow: hidden;
						background: #fff;

						.img {
							float: left;
							width: 232upx;
							height: 232upx;
							margin-right: 8upx;
							margin-bottom: 8upx;
							background: #333;
						}
					}

					.item_date {
						background: #fff;
						padding: 18upx 19upx 26upx 19upx;
						font-size: 24upx;
						line-height: 24upx;
						color: rgb(51, 51, 51);
					}
				}
			}

			.bottom_bar {
				.van-info {
					right: 3upx;
					top: -6px;
				}
			}
		}

		.discuss {
			.header {
				overflow: hidden;
				background: #fff;
				padding: 30upx 22upx;

				.header_label {
					float: left;
					font-size: 30upx;
					line-height: 30upx;
					color: rgb(40, 40, 40);
				}

				.header_value {
					float: right;
					font-size: 30upx;
					line-height: 30upx;
					color: rgb(102, 102, 102);
				}

				.header_icon {
					float: right;
					width: 16upx;
					height: 27upx;
					margin-left: 20upx;
				}
			}

			.item {
				.item_header {
					margin-top: 16upx;
					overflow: hidden;
					height: 80upx;
					background: #fff;

					.header_avatar {
						float: left;
						width: 58upx;
						height: 58upx;
						background: #333;
						border-radius: 50%;
						margin-left: 26upx;
						margin-top: 22upx;
					}

					.header_txt {
						float: left;
						font-size: 30upx;
						line-height: 30upx;
						color: rgb(51, 51, 51);
						margin-top: 40upx;
						margin-left: 20upx;
					}

					.header_time {
						float: left;
						font-size: 24upx;
						line-height: 24upx;
						color: rgb(102, 102, 102);
						margin-top: 42upx;
						margin-left: 30upx;
					}
				}

				.item_des {
					font-size: 30upx;
					line-height: 46upx;
					color: rgb(51, 51, 51);
					padding: 16upx 26upx;
					background: #fff;
				}

				.item_imgs {
					padding: 0 11upx 0 19upx;
					overflow: hidden;
					background: #fff;

					.img {
						float: left;
						width: 232upx;
						height: 232upx;
						margin-right: 8upx;
						margin-bottom: 8upx;
						background: #333;
					}
				}

				.item_date {
					background: #fff;
					padding: 18upx 19upx 26upx 19upx;
					font-size: 24upx;
					line-height: 24upx;
					color: rgb(51, 51, 51);
				}
			}
		}

		.goods {
			.goods_title {
				background: #fff;
				height: 66upx;
				font-size: 30upx;
				line-height: 66upx;
				padding-left: 20upx;
			}

			.goods_img {
				width: 750upx;
				height: 500upx;
				background: #333;
				vertical-align: bottom;
			}
		}
	}

	.attr {
		.popup_attr {
			.back {
				position: relative;
				height: 268upx;

				.img {
					z-index: 100;
					position: absolute;
					top: 0upx;
					left: 16upx;
					width: 240upx;
					height: 240upx;
					background: red;
					border-radius: 10upx;
				}

				.attr_top {
					z-index: 1;
					position: absolute;
					top: 80upx;
					left: 0upx;
					padding-top: 40upx;
					padding-bottom: 42upx;
					background: #fff;
					width: 750upx;
					height: 106upx;

					.top_middle {
						float: left;
						margin-left: 290upx;

						.des_price {
							font-size: 30upx;
							line-height: 30upx;
							color: #FF000D;
						}

						.des_count {
							font-size: 24upx;
							line-height: 24upx;
							color: #666;
							margin-top: 18upx;
							margin-bottom: 16upx;
						}

						.des_select {
							font-size: 22upx;
							line-height: 22upx;
							color: #333;
						}
					}

					.top_right {
						float: right;
						margin-right: 36upx;

						.right_close {
							width: 40upx;
							height: 40upx;
						}
					}
				}
			}

			.attr_gui {
				background: #fff;
				padding: 22upx 34upx 18upx 34upx;
				border-top: 1upx solid #f2f2f2;

				.gui_title {
					font-size: 24upx;
					line-height: 24upx;
					margin-bottom: 20upx;
				}

				.gui_list {
					overflow: hidden;

					.gui_item {
						float: left;
						width: 164upx;
						height: 58upx;
						line-height: 58upx;
						text-align: center;
						color: #333;
						font-size: 20upx;
						background: #F2F2F2;
						border-radius: 6upx;
						margin-left: 20upx;
					}

					.gactive {
						border: 1upx solid #FF000D;
						color: #FF000D;
						background: transparent;
					}
				}
			}

			.attr_color {
				background: #fff;
				padding: 22upx 34upx 18upx 34upx;
				border-top: 1upx solid #f2f2f2;

				.color_title {
					font-size: 24upx;
					line-height: 24upx;
					margin-bottom: 20upx;
				}

				.color_list {
					overflow: hidden;

					.color_item {
						float: left;
						width: 164upx;
						height: 58upx;
						line-height: 58upx;
						text-align: center;
						color: #333;
						font-size: 20upx;
						background: #F2F2F2;
						border-radius: 6upx;
						margin-left: 20upx;
						overflow: hidden;

						.item_img {
							margin-top: 6upx;
							margin-left: 8upx;
							float: left;
							width: 66upx;
							height: 46upx;
							background: #666;
						}

						.item_txt {
							float: left;
							font-size: 24upx;
							line-height: 24upx;
							margin-left: 12upx;
							margin-top: 18upx;
						}
					}

					.cactive {
						border: 1upx solid #FF000D;
						color: #FF000D;
						background: transparent;
					}
				}
			}

			.num {
				padding: 60upx 20upx 228upx 34upx;
				background: #fff;
				border-top: 1upx solid #f2f2f2;
				height: 60upx;

				.num_left {
					float: left;
					font-size: 24upx;
					line-height: 24upx;
					margin-top: 20upx;
				}

				.num_right {
					float: right;
				}
			}

			.bottoms {
				width: 750upx;
				height: 100upx;
				font-size: 24upx;
				line-height: 100upx;
				text-align: center;
				overflow: hidden;
				border-top: 1upx solid #f2f2f2;

				.bottoms_cart {
					float: left;
					width: 375upx;
					height: 100upx;
					line-height: 100upx;
					background: #fff;
				}

				.bottoms_buy {
					float: left;
					width: 375upx;
					height: 100upx;
					line-height: 100upx;
					background: #D41C1C;
					color: #fff;
				}
			}
		}
	}

	.popup_ping {
		width: 612rpx;
		height: 500rpx;
		border-radius: 30upx;
		background: #fff;
		margin: 0 auto;

		.ping_delete {
			text-align: right;
			padding-top: 28rpx;
			padding-right: 34rpx;
		}

		.ping_title {
			overflow: hidden;
			font-size: 30rpx;
			line-height: 30rpx;
			color: #333;
			text-align: center;
		}

		.ping_des {
			margin-top: 28rpx;
			font-size: 24rpx;
			line-height: 24rpx;
			color: #666666;
			text-align: center;
		}

		.ping_img {
			margin-top: 52rpx;

			.img1 {
				margin-left: 186rpx;
				width: 94rpx;
				height: 94rpx;
			}

			.img2 {
				margin-left: 82rpx;
				width: 94rpx;
				height: 94rpx;
			}
		}

		.ping_btn {
			width: 430rpx;
			height: 64rpx;
			margin: 0 auto;
			border-radius: 10rpx;
			font-size: 28rpx;
			line-height: 64rpx;
			text-align: center;
			margin-top: 64rpx;
			background: #FFD944;
		}

	}

	.popup_can {
		width: 578rpx;
		height: 772rpx;
		background: #fff;
		margin: 0 auto;
		position: relative;

		.can_title {
			padding: 37rpx 0;
			font-size: 30rpx;
			line-height: 30rpx;
			text-align: center;
			color: #333;
			border-bottom: 1rpx solid #f2f2f2;
		}

		.can_delete {
			position: absolute;
			top: 25rpx;
			right: 20rpx;
		}

		.can_item {
			overflow: hidden;
			border-bottom: 1rpx solid #f2f2f2;

			.item_left {
				float: left;
				margin-top: 28rpx;
				margin-left: 26rpx;

				.left_img {
					width: 74rpx;
					height: 74rpx;
				}
			}

			.item_middle {
				float: left;
				margin-left: 17rpx;

				.middle_top {
					margin-top: 30rpx;
					font-size: 26rpx;
					line-height: 26rpx;
					color: #333;

					.top_num {
						margin-left: 15rpx;
						color: #666;
					}
				}

				.middle_bottom {
					margin-top: 18rpx;
					font-size: 26rpx;
					line-height: 26rpx;
					color: #999;
				}
			}

			.item_right {
				float: right;
				margin-top: 33rpx;
				margin-right: 20rpx;
				width: 138rpx;
				height: 62rpx;
				line-height: 62rpx;
				text-align: center;
				font-size: 26rpx;
				color: #fff;
				background: #D41C1C;
				border-radius: 10rpx;

			}

		}
	}
</style>
