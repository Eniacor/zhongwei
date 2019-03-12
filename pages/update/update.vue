<template>
	<view>
		<view class="empty">
			<image class="img" src="/static/update.png"></image>
			<view class="txt">还没有更新哦，请稍后再来~</view>
		</view>
		<custom-popup show="true" type="middle">
			<view class="update">
				<image class="img" src="/static/update1.png"></image>
				<view class="version">
					<text class="version_txt">最新版本</text>
					<text class="version_num">V5.1.3</text>
				</view>
				<view class="des">
					发现新本版更多优化，界面全新设计，速度更快，效率更高，体验更好。
				</view>
				<view class="line"></view>
				<view class="btn">
					<view class="btn_cancle">取消</view>
					<view class="btn_line"></view>
					<view class="btn_update">立即更新</view>
				</view>
			</view>
		</custom-popup>
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
	.empty{
		.img{
			display: block;
			width: 421upx;
			height: 439upx;
			margin: 0 auto;
			margin-top:135upx;
		}
		.txt{
			font-size: 32upx;
			line-height: 32upx;
			color: #999;
			text-align: center;
			margin-top:73upx;
		}
	}
	.update{
		width: 578upx;
		height: 726upx;
		background: #fff;
		border-radius: 10upx;
		.img{
			display: block;
			width: 503upx;
			height: 409upx;
			margin:0 auto;
			margin-top:13upx;
		}
		.version{
			text-align: center;
			.version_txt{
				font-size: 24upx;
				color: rgb(24, 22, 22);
				margin-right: 14upx;
			}
			.version_num{
				display: inline-block;
				font-size: 20upx;
				line-height: 22upx;
				color:#fff;
				background: #357CEA;
				padding:1upx 8upx;
				border-radius: 10upx;
			}
		}
		.des{
			width: 420upx;
			font-size: 20upx;
			color: rgb(217,216,219);
			margin: 0 auto;
			line-height: 32upx;
			margin-top:18upx;
		}
		.line{
			width: 440upx;
			height: 2upx;
			background: #f2f2f2;
			margin: 0 auto;
			margin-top:62upx;
		}
		.btn{
			overflow: hidden;
			width:400upx;
			margin: 0 auto;
			padding:30upx 0;
			.btn_cancle{
				float: left;
				font-size: 30upx;
				color: rgb(126, 126, 130);
			}
			.btn_line{
				float: left;
				width: 2upx;
				height: 40upx;
				background: #FF8136;
				margin-left: 114upx;
				margin-right: 100upx;
				margin-top:4upx;
			}
			.btn_update{
				float:right;
				font-size: 30upx;
				color:#357CEA;
				
			}
		}
	}
</style>
