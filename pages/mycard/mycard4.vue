<template>
	<view class="index">
		<view class="top">
			<view class="name">
				<view class="name_left">银行卡</view>
				<view class="name_right">中国建设银行储蓄卡</view>
			</view>
			<view class="num">
				<view class="num_left">
					卡<text>号</text>
				</view>
				<view class="num_right">
					<text>6217</text>
					<text>0013</text>
					<text>2000</text>
					<text>3414</text>
					<text>614</text>
				</view>
			</view>
		</view>
		<view class="notice">提醒：后续只能绑定该持卡人的银行卡</view>
		<view class="form">
			<view class="form_lable">持卡人</view>
			<input class="form_value" placeholder="持卡人姓名"/>
		</view>
		<view class="form">
			<view class="form_lable">身份证</view>
			<input class="form_value" placeholder="请输入证据号码"/>
		</view>
		<view class="form">
			<view class="form_lable">手机号</view>
			<input class="form_value" placeholder="银行预留手机号"/>
		</view>
		<view class="look">
			<text class="look_a">查看</text>
			<text class="look_b">《用户协议》</text>
		</view>
		<view class="btn">同意协议并验证</view>
		<view class="des">信息加密处理，仅用于银行验证及实名</view>
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
	.top{
		background: #fff;
		.name{
			overflow: hidden;
			padding-top:54upx;
			padding-left:30upx;
			.name_left{
				float: left;
				font-size: 28upx;
				line-height: 28upx;
				color:rgb(40,40,40);
			}
			.name_right{
				float: left;
				font-size: 28upx;
				line-height: 28upx;
				color:rgb(40,40,40);
				margin-left: 34upx;
			}
		}
		.num{
			overflow: hidden;
			padding-top:26upx;
			padding-left:30upx;
			padding-bottom:50upx;
			.num_left{
				float: left;
				font-size: 28upx;
				line-height: 28upx;
				color:rgb(40,40,40);
				text{
					margin-left:30upx;
				}
			}
			.num_right{
				float: left;
				font-size: 28upx;
				line-height: 28upx;
				color:rgb(40,40,40);
				margin-left: 34upx;
			}
		}
	}
	.notice{
		padding-top:37upx;
		padding-left:32upx;
		padding-bottom:28upx;
		font-size: 24upx;
		line-height: 24upx;
		color:rgb(102,102,102);
	}
	.form{
		overflow: hidden;
		width: 100%;
		height: 106upx;
		background: #fff;
		.form_lable{
			margin-top:39upx;
			margin-left:32upx;
			float: left;
			font-size: 28upx;
			line-height:28upx;
		}
		.form_value{
			float: left;
			font-size: 28upx;
			margin-top:25upx;
			margin-left:38upx;
		}
	}
	.look{
		margin-top:44upx;
		margin-left:25upx;
		.look_a{
			font-size: 24upx;
			line-height: 24upx;
		}
		.look_b{
			font-size: 24upx;
			line-height: 24upx;
			color: #255DA8;
			margin-left:10upx;
		}
	}
	.btn{
		width: 700upx;
		height: 90upx;
		border-radius: 10upx;
		background: rgb(255,217,68);
		margin: 0 auto;
		text-align: center;
		line-height: 90upx;
		margin-top:63upx;
	}
	.des{
		font-size: 24upx;
		line-height: 24upx;
		margin-left:25upx;
		margin-top:36upx;
		color: rgb(102,102,102);
	}
	
</style>
