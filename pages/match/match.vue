<template>
	<view>
		<view class="contant">
			<view class="pro">
				<text class="pro_txt">您的专业</text>
				<text class="pro_icon">
					<uni-icon size="18" type="arrowdown" color="#696969"></uni-icon>
				</text>
				<text class="pro_input">请选择</text>
			</view>
			<view class="title">请选择朋友圈典型群体（可多选）</view>
			<view class="content">
				<view class="item">公务员</view>
				<view class="item">公务员</view>
				<view class="item">公务员</view>
				<view class="item">公务员</view>
				<view class="item">公务员</view>
				<view class="item">公务员</view>
				<view class="item">公务员</view>
				<view class="item">公务员</view>
				<view class="item">公务员</view>
				<view class="item">公务员</view>
				<view class="item">公务员</view>
				<view class="item">公务员</view>
				<view class="item">公务员</view>
			</view>
			<view class="add">完成注册</view>
		</view>
	</view>
</template>

<script>
	import uniSegmentedControl from '../../components/uni-segmented-control.vue';
	import uniIcon from '../../components/uni-icon.vue';
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
	page{
		background: #F3FAFC;
	}
	.pro {
		padding-top:50upx;
		padding-bottom:32upx;
		overflow: hidden;
		margin-left:42upx;
		margin-right:36upx;
		border-bottom: 2upx solid #f2f2f2;
		.pro_txt{
			float: left;
			font-size: 34upx;
			line-height: 34upx;
			color: #000;
		}
		.pro_input {
			float:right;
			font-size: 30upx;
			line-height: 30upx;
			color: rgb(204, 204, 204);
		}
		.pro_icon{
			float: right;
			margin-left: 28upx;
			font-size: 30upx;
			line-height: 30upx;
		}
	}
	.title{
		font-size: 34upx;
		line-height: 34upx;
		color:#000;
		padding-top:63upx;
		padding-bottom:32upx;
		margin-left:42upx;
		margin-right:36upx;
		border-bottom: 2upx solid #f2f2f2;
	}
	.content{
		
		padding:32upx 42upx;
		.item{
			display: inline-block;
			width: 142upx;
			height: 52upx;
			line-height: 52upx;
			text-align: center;
			font-size: 24upx;
			// padding:10upx 24upx;
			border:2upx solid #CCCCCC;
			border-radius:30upx;
			margin-bottom: 30upx;
			margin-left: 14upx;
			 
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
		margin-top:209upx;
		color: rgb(44, 44, 44);
		border-radius: 10upx;
	}
</style>
