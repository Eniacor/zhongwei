<template>
	<view>
		<view style="background: #FED943;">
			<uni-segmented-control :current="current" :values="items" activeColor="#000" v-on:clickItem="onClickItem">
			</uni-segmented-control>
		</view>
		<view class="content">
			<view v-show="current === 0">
				<view class="contant1">
					<view class="mobile">
						<input type="text" placeholder="请输入手机号">
					</view>
					<view class="line"></view>
					<view class="password">
						<input class="input" type="text" placeholder="请输入验证码">
						<text class="btn">获取验证码</text>
					</view>
					<view class="add">登录</view>
					<view class="des">
						<text class="des_left">还没有账号?</text>
						<text class="des_right">立即注册</text>
					</view>
					<view class="other">其他方式登录</view>
					<view class="author">
						<view class="item">
							<image class="qq" src="/static/add2.png"></image>
							<text class="txt">QQ登录</text>
						</view>
						<view class="line"></view>
						<view class="item">
							<image class="wechat" src="/static/add4.png"></image>
							<text class="txt">微信登录</text>
						</view>
						<view class="line"></view>
						<view class="item">
							<image class="webo" src="/static/add3.png"></image>
							<text class="txt">微博登录</text>
						</view>
					</view>
				</view>
			</view>
			<view v-show="current === 1">
				<view class="contant2">
					
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import uniSegmentedControl from '../../components/uni-segmented-control.vue';
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
	.contant1{
		.mobile{
			width: 550upx;
			background: #fff;
			padding:32upx 54upx;
			input{
				font-size: 22upx;
			}
			margin: 0 auto;
			margin-top:42upx;
		}
		.line{
			width:500upx;
			height: 1upx;
			background: #f2f2f2;
		}
		.password{
			width: 590upx;
			background: #fff;
			padding:32upx 54upx;
			padding-right: 14upx;
			overflow: hidden;
			input{
				float: left;
				font-size: 22upx;
			}
			.btn{
				float: right;
				padding:16upx 22upx;
				background: #FFD945;
				font-size: 22upx;
				line-height: 22upx;
			}
			margin: 0 auto;
		}
		.add{
			width: 660upx;
			height: 98upx;
			line-height: 98upx;
			font-size: 28upx;
			text-align: center;
			background: #FFD945;
			margin: 0 auto;
			margin-top:80upx;
			color: rgb(44, 44, 44);
		}
		.des{
			text-align: center;
			margin-top:39upx;
			line-height: 24upx;
			.des_left{
				font-size: 24upx;
				line-height: 24upx;
				color: rgb(142, 142, 142);
			}
			.des_right{
				font-size: 24upx;
				line-height: 24upx;
				margin-left:10upx;
				color: rgb(142, 142, 142);
			}
		}
		.other{
			margin-top:502upx;
			font-size: 24upx;
			line-height: 24upx;
			text-align: center;
			color: rgb(65, 65, 65);
		}
		.author{
			margin-top:67upx;
			overflow: hidden;
			.item{
				float: left;
				.qq{
					float: left;
					width: 24upx;
					height: 28upx;
					margin-left: 97upx;
				}
				.wechat{
					float: left;
					width:32upx;
					height: 28upx;
				}
				.webo{
					float: left;
					width: 32upx;
					height: 28upx;
				}
				.txt{
					float: left;
					font-size: 22upx;
					line-height: 22upx;
					margin-left: 16upx;
					margin-top:4upx;
				}
			}
			.line{
				float: left;
				width: 1upx;
				height: 32upx;
				background: #000;
				margin-left: 32upx;
				margin-right: 32upx;
			}
		}
	}
</style>
