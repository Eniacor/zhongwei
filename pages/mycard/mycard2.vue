<template>
	<view>
		<view class="back">
			<view class="card_title">请输入手机152****0903</view>
			<view class="card_content">
				<view class="content_lable">验证码</view>
				<input class="content_name" value="015137" />
				<view class="content_icon">
					<uni-icon size="24" type="clear" color="#999"></uni-icon>
				</view>
				<view class="content_line"></view>
				<view class="content_num">(46)</view>
				<view class="content_btn">重新获取</view>
			</view>
			<view class="card_notice" @click="showCodePopup">收不到验证码？</view>
		</view>
		<navigator url="/pages/mycard/mycard4"  hover-class="none">
			<view class="card_btn">下一步</view>
		</navigator>
		
		
		<custom-popup :show="showPopupCode" type="middle" v-on:hidePopup="hidePopup">
			<view class="popup_content">
				<view class="content_title">收不到验证码？</view>
				<view class="content_content">
					<view class="content_item">
						1.请确认152****0903是否中国建设银行**46411尾号银行卡的
						预留手机号码
					</view>
					<view class="content_item">
						2.请确认是否中国建设银行尾号银行卡的
					</view>
					<view class="content_item">
						3.请确认152****0903是否中国建设银行**46411尾号银行卡的
						预留手机号码
					</view>
					<view class="content_item">
						4.请确认152****0903是否中国建设银行**46411尾号银行卡的
						预留手机号码
					</view>
					<view class="content_item">
						5.请确认是否中国建设银行尾号银行卡的
					</view>
				</view>
				<view class="content_bottom">知道了</view>
			</view>
		</custom-popup>
	</view>
</template>

<script>
	import customPopup from '../../components/custom-popup.vue';
	import uniIcon from '../../components/uni-icon.vue'
	export default {
		data() {
			return {
				showPopupCode:false,
			};
		},
		components: {
			customPopup,
			uniIcon
		},
		methods:{
			//统一的关闭popup方法
			hidePopup: function() {
				this.showPopupCode = false;
			},
			//展示居中 popup
			showCodePopup: function() {
				this.hidePopup();
				this.showPopupCode = true;
			},
		}
	}
</script>

<style lang="scss">
	.back{
		background: #fff;
		height: 315upx;
	}
	.card_title{
		padding-top:54upx;
		padding-left:35upx;
		font-size: 28upx;
		line-height: 28upx;
		color: #000;
		text-align: center;
	}
	.card_content{
		width: 686upx;
		height: 72upx;
		margin: 0 auto;
		background:rgba(195,195,195,.24);
		border-radius: 14upx;
		overflow: hidden;
		margin-top:53rpx;
		.content_lable{
			float: left;
			font-size: 30upx;
			line-height:30upx;
			color:rgb(40,40,40);
			margin:20upx 0 0 20upx;
		}
		.content_name{
			width:246upx;
			float: left;
			font-size: 30upx;
			line-height:30upx;
			margin:8upx 0 0 30upx;
		}
		.content_icon{
			float:left;
			margin-top:12upx;
		}
		.content_line{
			float:left;
			width: 1upx;
			height: 48upx;
			background: #C9C9C9;
			margin-top:14upx;
			margin-left:16upx;
			margin-right: 24upx;
		}
		.content_num{
			float:left;
			margin-top:14upx;
		}
		.content_btn{
			float:left;
			margin-top:14upx;
			margin-left: 22upx;
		}
	}
	.card_name{
		margin-top:21upx;
		margin-left:52upx;
		.name_icon{
			width: 40upx;
			height: 40upx;
			border-radius: 50%;
			background:#FFD944;
			vertical-align: middle;
		}
		.name_txt{
			font-size: 20upx;
			line-height: 20upx;
			color: rgb(102,102,102);
			margin-left: 22upx;
		}
	}
	.card_notice{
		font-size: 24upx;
		line-height: 24upx;
		text-align: right;
		margin-top:40upx;
		margin-bottom:40upx;
		margin-right: 36upx;
		color: #4669A2;
	}
	.card_btn{
		width: 682upx;
		height: 80upx;
		background: #FFD944;
		border-radius: 10upx;
		font-size: 30upx;
		line-height:80upx;
		text-align: center;
		margin: 0 auto;
		margin-top:90upx;
	}
	
	.popup_content{
		width: 624upx;
		height: 582upx;
		background: #fff;
		border-radius: 16upx;
		.content_title{
			font-size: 36upx;
			line-height: 36upx;
			color:#000;
			text-align: center;
			margin-top: 48upx;
			margin-bottom: 48upx;
		}
		.content_content{
			padding:0 44upx;
			.content_item{
				font-size: 30upx;
				line-height: 40upx;
				color:rgb(102,102,102);
			}
		}
		.content_bottom{
			border-top: 1upx solid #f2f2f2;
			font-size: 36upx;
			line-height: 100upx;
			text-align: center;
			margin-top:30upx;
		}
	}
</style>
