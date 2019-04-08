<template>
	<view>
		<view class="bank">
			<image class="bank_img" src=""></image>
			<view class="bank_txt">尾号666</view>
		</view>
		<view class="balance">
			<view class="balance_txt">可提先金额：</view>
			<view class="balance_value">12,100.00</view>
			<view class="balance_txt">元</view>
		</view>
		<view class="money">
			<view class="money_dot">￥</view>
			<input class="money_value" value="12,100.00" />
			<view class="money_txt">全部提现</view>
		</view>
		<view class="des">
			本月还可免费提现三笔
		</view>
		<view class="btn">
			确认提现
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
	.bank{
		position: relative;
		width: 690upx;
		height: 138upx;
		margin: 0 auto;
		margin-top:24upx;
		.bank_img{
			width: 690upx;
			height: 138upx;
			background: #999;
			border-radius: 10upx;
		}
		.bank_txt{
			position: absolute;
			top: 36upx;
			left:200upx;
			font-size: 36upx;
			line-height: 36upx;
			color:rgb(255,255,255);
		}
	}
	.balance{
		overflow: hidden;
		margin-top:82upx;
		.balance_txt{
			float: left;
			font-size: 24upx;
			line-height: 36upx;
			color: rgb(166, 171, 181);
			&:first-child{
				margin-left: 30upx;
			}
		}
		.balance_value{
			float: left;
			font-size: 36upx;
			line-height: 36upx;
			color: rgb(4, 148, 255);
		}
	}
	.money{
		display: flex;
		width: 690upx;
		margin: 0 auto;
		margin-top:65upx;
		padding-bottom:38upx;
		border-bottom:1upx solid rgb(4, 148, 255);
		.money_txt{
			width: 160upx;
			font-size: 27upx;
			color: rgb(86,93, 105);
		}
		.money_value{
			font-size: 36upx;
			line-height: 36upx;
			color: rgb(86,93,105);
		}
	}
	.des{
		margin-top:29upx;
		margin-left:30upx;
		font-size: 24upx;
		line-height: 24upx;
		color: rgb(166,171,181);
		margin-bottom:121upx;
	}
	.btn{
		
		width: 698upx;
		height: 92upx;
		margin:0 auto;
		font-size: 35upx;
		line-height: 92upx;
		color: rgb(0, 0, 0);
		text-align: center;
		border-radius: 10upx;
		background: #FFD944;

	}
</style>
