<template>
	<view>
		<view class="contant1">
			<view class="avatar">
				<view class="img"></view>
			</view>
			<view class="mobile">
				<input type="text" placeholder="请输入手机号">
				<text class="mobile_icon">
					<uni-icon size="32" type="clear" color="#0ED485"></uni-icon>
				</text>
			</view>
			<view class="code">
				<view class="code_left">
					<input class="input" type="text" placeholder="请输入验证码">
				</view>
				<view class="code_right">获取验证码</view>
			</view>
			<view class="mobile">
				<input type="text" placeholder="请输入新密码">
				<image class="icon_eye" src="/static/password1.png"></image>
			</view>
			<view class="add">下一步</view>
		</view>
	</view>
</template>

<script>
	import uniSegmentedControl from '../../components/uni-segmented-control.vue';
	import uniIcon from '../../components/uni-icon.vue'
	export default {
		data() {
			return {
				items: [
					'快捷登录',
					'密码登录'
				],
				current: 0,
			};
		},
		components: {
			uniSegmentedControl,
			uniIcon
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
	.avatar {
		width: 178upx;
		height: 178upx;
		border-radius: 50%;
		background: #fff;
		margin: 0 auto;
		margin-top: 160upx;
		margin-bottom: 128upx;
		border: 1upx solid #EFEFF0;

		.img {
			width: 136upx;
			height: 136upx;
			background: #FFD945;
			border-radius: 50%;
			margin-top: 21upx;
			margin-left: 21upx;
		}
	}

	.mobile {
		display: flex;
		justify-content: space-between;
		align-items: center;
		width:606upx;
		height: 108upx;
		border-radius: 10upx;
		border: 1upx solid #E3E4E5;
		input {
			float: left;
			margin-left:32upx;
			font-size: 30upx;
		}
		.mobile_icon{
			float: right;
			margin-right:37upx;
		}
		.icon_eye{
			margin-right:37upx;
			width: 40upx;
			height: 20upx;
		}
		margin: 0 auto;
	}
	.code{
		width:608upx;
		height: 110upx;
		margin:0 auto;
		margin-top:39upx;
		margin-bottom:39upx;
		.code_left{
			float: left;
			width:348upx;
			height: 108upx;
			border-radius: 10upx;
			border: 1upx solid #E3E4E5;
			input {
				float: left;
				margin-top: 29upx;
				margin-left:32upx;
				font-size: 30upx;
			}
		}
		.code_right{
			float:right;
			width:222upx;
			height: 108upx;
			text-align: center;
			line-height: 108upx;
			border-radius: 10upx;
			border: 1upx solid #4768F3;
			font-size: 30upx;
			color:#4768F3;
		}
	}
	.add {
		width: 608upx;
		height: 98upx;
		line-height: 98upx;
		font-size: 28upx;
		text-align: center;
		background: #FFD945;
		margin: 0 auto;
		margin-top: 40upx;
		color: rgb(44, 44, 44);
		border-radius: 10upx;
	}
</style>
