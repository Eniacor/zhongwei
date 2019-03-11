<template>
	<view class="index">
		<view class="item">
			<view class="item_left"></view>
			<view class="item_right">
				<view class="right_title">中国建设银行</view>
				<view class="right_des">储蓄卡</view>
				<view class="right_num">
					<text>****</text>
					<text>****</text>
					<text>****</text>
					<text>4614</text>
				</view>
			</view>
		</view>
		<view class="add">
			<navigator url="/pages/mycard/mycard"  hover-class="none">
				<image class="add_img" src="/static/cardadd.png"></image>
				<view class="add_txt">添加银行卡</view>
			</navigator>
			
		</view>
	</view>
</template>

<script>
	import customPopup from '../../components/custom-popup.vue';
	export default {
		data() {
			return {
				
			};
		},
		components: {
			customPopup
		},
	}
</script>

<style lang="scss">
	.item{
		width: 714upx;
		height: 212upx;
		border: 1upx solid transparent;
		border-radius: 20upx;
		background: #fff;
		margin:0 auto;
		margin-top:15upx;
		.item_left{
			float: left;
			width: 69upx;
			height: 69upx;
			border-radius: 50%;
			background: #FFD944;
			margin-top:40upx;
			margin-left:47upx;
		}
		.item_right{
			float: left;
			margin-top:41upx;
			margin-left: 41upx;
			.right_title{
				font-size: 30upx;
				line-height: 30upx;
				color: #000;
			}
			.right_des{
				font-size: 24upx;
				line-height: 24upx;
				margin-top:17upx;
				margin-bottom:37upx;
				color: #000;
			}
			.right_num{
				text{
					font-size: 24upx;
					line-height: 24upx;
					color: #000;
					margin-right:41upx;
				}
			}
		}
	}
	.add{
		width: 714upx;
		height: 138upx;
		margin:0 auto;
		background: #fff;
		border-radius: 20upx;
		margin-top:15upx;
		border:1upx solid transparent;
		.add_img{
			display: block;
			width: 52upx;
			height: 52upx;
			margin: 0 auto;
			margin-top:26upx;
		}
		.add_txt{
			font-size: 24upx;
			line-height: 24upx;
			text-align: center;
			margin-top:18upx;
		}
	}
</style>
