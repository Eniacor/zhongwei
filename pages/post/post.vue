<template>
	<view>
		<view class="top">
			<view class="top_left"></view>
			<view class="top_right">
				<view class="right_title">MacBookPro 2018款星空灰色32G...</view>
				<view class="right_bottom">
					<text class="bottom_left">数量8</text>
					<text class="bottom_right">实收款：￥20000</text>
				</view>
			</view>
		</view>
		<view class="brand">
			<view class="brand_left"></view>
			<view class="brand_right">
				<view class="right_title">顺丰快递</view>
				<view class="right_bottom">
					<text class="bottom_left">物流单号：SF568956214</text>
					<text class="bottom_right">复制</text>
				</view>
			</view>
		</view>
		<view class="uni-timeline">
			<view class="uni-timeline-item uni-timeline-first-item">
				<view class="uni-timeline-item-divider"></view>
				<view class="uni-timeline-item-content">
					<view class="txt">宿迁</view>
					<view class="datetime">2018.05</view>
				</view>
			</view>
			<view class="uni-timeline-item">
				<view class="uni-timeline-item-divider"></view>
				<view class="uni-timeline-item-content">
					<view class="txt">淮安</view>
					<view class="datetime">2018.07</view>
				</view>
			</view>
			<view class="uni-timeline-item uni-timeline-last-item">
				<view class="uni-timeline-item-divider"></view>
				<view class="uni-timeline-item-content">
					<view class="txt">上海</view>
					<view class="datetime">2018.10</view>
				</view>
			</view>
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
	.top{
		overflow: hidden;
		padding:16upx 0;
		background: #fff;
		.top_left{
			float: left;
			width: 140upx;
			height: 140upx;
			border-radius: 10upx;
			background: darkgoldenrod;
			margin-left:44upx;
		}
		.top_right{
			float: left;
			margin-left: 25upx;
			.right_title{
				font-size: 30upx;
				line-height: 30upx;
				color: rgb(40, 40, 40);
				margin-top: 30upx;
			}
			.right_bottom{
				margin-top: 27upx;
				line-height:24upx;
				overflow: hidden;
				.bottom_left{
					float: left;
					font-size: 24upx;
					line-height:24upx;
					color: rgb(101,101,101);
				}
				.bottom_right{
					float: right;
					font-size: 24upx;
					line-height:24upx;
					color: rgb(101,101,101);
				}
			}
		}
	}
	.brand{
		overflow: hidden;
		padding:30upx 0;
		background: #fff;
		margin-top:16upx;
		.brand_left{
			float: left;
			width:115upx;
			height:115upx;
			background: darkgoldenrod;
			margin-left:60upx;
		}
		.brand_right{
			float: left;
			margin-left: 28upx;
			.right_title{
				font-size: 30upx;
				line-height: 30upx;
				color: #000;
				margin-top:16upx;
			}
			.right_bottom{
				margin-top: 25upx;
				line-height:30upx;
				position: relative;
				width: 502upx;
				.bottom_left{
					font-size: 30upx;
					line-height:30upx;
					color: #000;
				}
				.bottom_right{
					position: absolute;
					top: 0;
					right:0;
					font-size: 24upx;
					line-height:24upx;
					color: #000;
					padding: 10upx 22upx;
					border-radius: 30upx;
					color: #000;
					box-shadow:0px 0px 10px #CBCBCB;
				}
			}
		}
	}
	.uni-timeline{
		padding: 68upx 117upx 0 86upx;
		margin: 0;
		.uni-timeline-item{
			.uni-timeline-item-divider{
				width: 15upx;
				height: 15upx;
				&::before{
					left: 3px;
				}
				&::after{
					left: 3px;
				}
			}
			.uni-timeline-item-content{
				padding-left: 112upx;
				width: 444upx;
				.txt{
					font-size: 24upx;
					line-height: 36upx;
				}	
				.datetime{
					font-size: 20upx;
					line-height:20upx;
					margin-top:20upx;
				}
			}
		}
		.uni-timeline-first-item .uni-timeline-item-divider {
			background-color: #333333;
		}
		.uni-timeline-item .uni-timeline-item-divider{
			background-color: #333333;
		}
		.uni-timeline-last-item .uni-timeline-item-divider {
			background-color: #333333;
		}
	}
</style>
