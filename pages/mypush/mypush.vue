<template>
	<view class="page">
		<view class="top_header" style="padding-left: 35upx;background: #fff;">
			<custom-segmented-control 
				:current="current" 
				:values="items" 
				v-on:clickItem="onClickItem" >
			</custom-segmented-control>
		</view>
		<view class="top_content">
			<view v-show="current === 0">
				<view class="sucai">
					<view class="item">
						<view class="item_header">
							<image class="header_avatar"></image>
							<view class="header_txt">环球小荐人</view>
							<view class="header_time">4小时前发布</view>
						</view>
						<view class="item_des">
							普通的眼罩你肯定见过，那蒸汽眼罩你见过？
							普通的眼罩你肯定见过，那蒸汽眼罩你见过？
							普通的眼罩你肯定见过，那蒸汽眼罩你见过？
							普通的眼罩你肯定见过，那蒸汽眼罩你见过？
						</view>
						<view class="item_imgs">
							<image class="img"></image>
							<image class="img"></image>
							<image class="img"></image>
							<image class="img"></image>
							<image class="img"></image>
						</view>
						<view class="item_bottom">
							<view class="bottom_item">
								<image class="item_img" src="/static/push1.png"></image>
								<text class="item_txt">14人收藏</text>
							</view>
							<view class="bottom_item">
								<image class="item_img" src="/static/push2.png"></image>
								<text class="item_txt">分享</text>
							</view>
							<view class="bottom_item">
								<image class="item_img" src="/static/push3.png"></image>
								<text class="item_txt">14</text>
							</view>
						</view>
					</view>
				</view>
			</view>
			<view v-show="current === 1">
				<view class="book">
					<view class="book_left">
						<view class="left_title">
							在学校如何潜移默化推广销售
						</view>
						<view class="left_bottom">
							<text class="bottom_name">柏林</text>
							<text class="bottom_date">2019-01-23</text>
							<image class="bottom_icon" src="/static/push6.png" ></image>
							<text class="bottom_num">128</text>
						</view>
					</view>
					<view class="book_right">
						<image class="right_img" src="" ></image>
					</view>
				</view>
				<view class="book">
					<view class="book_left">
						<view class="left_title">
							在校园如何潜移默化做推广销售
						</view>
						<view class="left_bottom">
							<text class="bottom_name">柏林</text>
							<text class="bottom_date">2019-01-23</text>
							<image class="bottom_icon" src="/static/push6.png" ></image>
							<text class="bottom_num">128</text>
						</view>
					</view>
					<view class="book_right">
						<image class="right_img" src="" ></image>
					</view>
				</view>
			</view>
		</view>
		<view class="menu">
			<view class="menu_item">
				<image class="item_icon" src="/static/push4.png"></image>
				<view class="item_txt">发布素材</view>
			</view>
			<view class="menu_item back">
				<image class="item_icon" src="/static/push4.png"></image>
				<view class="item_txt">发布笔记</view>
			</view>
		</view>
	</view>
</template>

<script>
	import customSegmentedControl from '../../components/custom-segmented-control.vue';
	export default {
		data() {
			return {
				items: [
					'卖货素材',
					'成功笔记',
				],
				current: 0,
			};
		},
		components: {
			customSegmentedControl,
		},
		methods:{
			onClickItem(index) {
				if (this.current !== index) {
					this.current = index;
				}
			},
		}
	}
</script>

<style lang="scss">
	page {
		position: relative;
	}
	.sucai{
		border-top: 1upx solid #f2f2f2;
		.item{
			.item_header{
				overflow: hidden;
				height: 80upx;
				background: #fff;
				.header_avatar{
					float: left;
					width: 58upx;
					height: 58upx;
					background: #333;
					border-radius: 50%;
					margin-left:26upx;
					margin-top:22upx;
				}
				.header_txt{
					float: left;
					font-size: 30upx;
					line-height: 30upx;
					color:rgb(51, 51, 51);
					margin-top:40upx;
					margin-left:20upx;
				}
				.header_time{
					float: left;
					font-size: 24upx;
					line-height:24upx;
					color:rgb(102, 102, 102);
					margin-top:42upx;
					margin-left:30upx;
				}
			}
			.item_des{
				font-size: 30upx;
				line-height: 46upx;
				color:rgb(51, 51, 51);
				padding:16upx 26upx;
				background: #fff;
			}
			.item_imgs{
				padding:0 11upx 0 19upx;
				overflow: hidden;
				background: #fff;
				.img{
					float: left;
					width: 232upx;
					height: 232upx;
					margin-right: 8upx;
					margin-bottom: 8upx;
					background: #333;
				}
			}
			.item_bottom{
				background: #fff;
				padding:40upx 0upx 40upx 0upx;
				
				font-size: 24upx;
				line-height: 24upx;
				color: rgb(51, 51, 51);
				overflow: hidden;
				.bottom_item{
					float: left;
					width: 250upx;
					text-align:center;
					.item_img{
						width: 30upx;
						height: 30upx;
						margin-right: 20upx;
					}
				}
			}
		}
	}
	.menu{
		position: absolute;
		top:0;
		right:0;
		width: 300upx;
		height:244upx;
		border-radius: 20upx;
		box-shadow:0px 0px 10px #EBEBEB;
		.menu_item{
			width: 100%;
			height: 122upx;
			background: #fff;
			overflow: hidden;
			border-bottom: 1upx solid #f2f2f2;
			.item_icon{
				float: left;
				width: 36upx;
				height:36upx;
				margin-top:46upx;
				margin-left:28upx;
			}
			.item_txt{
				float: left;
				font-size: 30upx;
				line-height: 30upx;
				font-weight: bold;
				margin-top:51upx;
				margin-left:32upx;
			}
		}
		.back{
			background: rgb(242, 242, 242);
		}
		
	}
	.book{
		overflow: hidden;
		background: #fff;
		height: 258upx;
		border: 1upx solid transparent;
		border-top-color:#f2f2f2;
		.book_left{
			float: left;
			margin-top:55upx;
			margin-left:45upx;
			.left_title{
				width: 384upx;
				height:88upx;
				font-size:32upx;
				line-height:46upx;
				color: rgb(0,0,0);
			}
			.left_bottom{
				width: 388upx;
				line-height:22upx;
				margin-top:25upx;
				.bottom_name{
					font-size:22upx;
					line-height:22upx;
					color:#666;
					margin-right: 12upx;
				}
				.bottom_date{
					font-size:22upx;
					line-height:22upx;
					color:#666;
				}
				.bottom_icon{
					width: 26upx;
					height: 20upx;
					margin-right: 10upx;
					margin-left:102upx;
				}
				.bottom_num{
					font-size:22upx;
					line-height:22upx;
					color:#333;
				}
			}
		}
		.book_right{
			float: right;
			margin-top:36upx;
			margin-right: 30upx;
			width: 226upx!important;
			height: 154upx!important;
			background: #666;
			border-radius: 10upx;
		}
		&:first-child{
			margin-top:25upx;
		}
	}
</style>
