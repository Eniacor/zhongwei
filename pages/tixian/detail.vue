<template>
	<view style="padding-top:25upx;">
		<view class="item">
			<view class="item_top">
				<view class="top_left">银联（4614）</view>
				<view class="top_right">￥135.00</view>
			</view>
			<view class="item_bottom">
				<view class="bottom_left">
					<image class="left_img" src="/static/time.png"></image>
					<text class="left_txt">2019-01-15 17:40</text>
				</view>
				<view class="bottom_right">
					<uni-icon size="18" type="checkbox-filled" color="#09BB07"></uni-icon>
					<text class="right_txt">转出成功</text>
				</view>
			</view>
		</view>
		<view class="item">
			<view class="item_top">
				<view class="top_left">银联（4614）</view>
				<view class="top_right">￥135.00</view>
			</view>
			<view class="item_bottom">
				<view class="bottom_left">
					<image class="left_img" src="/static/time.png"></image>
					<text class="left_txt">2019-01-15 17:40</text>
				</view>
				<view class="bottom_right">
					<uni-icon size="18" type="checkbox-filled" color="#09BB07"></uni-icon>
					<text class="right_txt">转出成功</text>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import uniIcon from '../../components/uni-icon.vue'
	export default {
		data() {
			return {
				
			};
		},
		components: {
		    uniIcon
		},
	}
</script>

<style lang="scss">
	.item{
		width:658upx;
		height: 154upx;
		background: #fff;
		border-radius: 12upx;
		margin: 0 auto;
		padding:36upx 28upx 0 34upx;
		margin-bottom: 10upx;
		.item_top{
			overflow: hidden;
			.top_left{
				float: left;
				font-size: 34upx;
				line-height: 34upx;
			}
			.top_right{
				float: right;
				font-size: 34upx;
				line-height: 34upx;
			}
		}
		.item_bottom{
			overflow: hidden;
			.bottom_left{
				float: left;
				margin-top: 71upx;
				.left_img{
					float: left;
					width:28upx;
					height:28upx;
				}
				.left_txt{
					float: left;
					font-size:24upx;
					line-height:24upx;
					color:rgb(101, 101, 101);
					margin-left: 12upx;
				}
			}
			.bottom_right{
				float: right;
				margin-top: 60upx;
				.right_txt{
					font-size:24upx;
					line-height:24upx;
					color:rgb(0,0,0);
					margin-left: 12upx;
				}
			}
		}
	}
	
</style>
