<template>
	<view>
		<view class="address">
			<view class="address_list">
				<view class="list_item">
					<view class="item_left">
						<view class="left_top">
							<text class="top_name">收货人：柏林</text>
							<text class="top_mobile">15251130905</text>
						</view>
						<view class="left_middle">
							收货地址：江苏省盐城市亭湖区盐城工学院新校区18栋三单元606-2
						</view>
					</view>
					<view class="item_middle"></view>
					<view class="item_right">
						<image class="right_arrow disblock" src="/static/gou.png"></image>
					</view>
				</view>
				<view class="list_item">
					<view class="item_left">
						<view class="left_top">
							<text class="top_name">收货人：柏林</text>
							<text class="top_mobile">15251130905</text>
						</view>
						<view class="left_middle">
							收货地址：江苏省盐城市亭湖区盐城工学院新校区18栋三单元606-2
						</view>
					</view>
					<view class="item_middle"></view>
					<view class="item_right">
						<image class="right_arrow" src="/static/gou.png"></image>
					</view>
				</view>
			</view>
			<view class="empty">
				<image class="empty_img" src="/images/static/empty_address.png"></image>
				<view class="empty_txt">暂无收货地址哦～</view>
			</view>
			<navigator hover-class="none" url="/pages/address/edit">
				<view class="btn">新增地址</view>
			</navigator>
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
	.address {
		.address_list {
			background: #f9f9f9;

			.list_item {
				background: #fff;
				overflow: hidden;
				border-bottom: 1upx solid #f2f2f2;

				.item_left {
					float: left;
					width: 580upx;
					padding: 40upx 32upx;

					.left_top {
						overflow: hidden;

						.top_name {
							float: left;
							font-size: 32upx;
							line-height: 32upx;
							color: rgb(51, 51, 51);
						}

						.top_mobile {
							float: right;
							font-size: 32upx;
							line-height: 32upx;
							color: rgb(51, 51, 51);
						}
					}

					.left_middle {
						margin-top: 24upx;
						font-size: 24upx;
						line-height: 30upx;
						color: #737373;
						height: 54upx;
					}
				}

				.item_middle {
					float: left;
					width: 1upx;
					height: 88upx;
					background: #CBCBCB;
					margin-top: 46upx;
				}

				.item_right {
					float: left;
					padding-top: 74upx !important;
					padding-left: 34upx !important;
					width: 68upx;
					height: 114upx;

					.right_arrow {
						display: none;
						width: 40upx;
						height: 40upx;
					}

					.disblock {
						display: block;
					}
				}

				&:last-child {}
			}
		}

		.empty {
			.empty_img {
				width: 632upx;
				height: 464upx;
				margin: 0 auto;
				margin-left: 53upx;
				margin-top: 356upx;
			}

			.empty_txt {
				font-size: 30upx;
				line-height: 30upx;
				text-align: center;
				color: #707070;
			}
		}

		.btn {
			position: fixed;
			bottom: 0;
			width: 750upx;
			height: 86upx;
			line-height: 86upx;
			background: #FFD944;
			color: rgb(51, 51, 51);
			outline: none;
			font-size: 30upx;
			text-align: center;
		}
	}
</style>
