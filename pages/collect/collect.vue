<template>
	<view>
		<view class="">
			<uni-segmented-control 
				:current="current" 
				:values="items" 
				v-on:clickItem="onClickItem" >
			</uni-segmented-control>
		</view>
		<view class="content">
			<view v-show="current === 0">
				<view class="collect">
					<view class="list">
						<view class="item">
							<view class="item_left">
								<image class="left_img" src=""></image>
							</view>
							<view class="item_right">
								<view class="right_title">小米 红米6 Pro 全网通手机 双卡双...</view>
								<view class="right_des">规格4+32G 颜色：巴黎蓝</view>
								<view class="right_count">库存紧张</view>
								<view class="right_price">￥118</view>
								<image class="right_delete" src="/static/delete.png" ></image>
							</view>
						</view>
						<view class="item">
							<view class="item_left">
								<image class="left_img" src=""></image>
							</view>
							<view class="item_right">
								<view class="right_title">小米 红米6 Pro 全网通手机 双卡双...</view>
								<view class="right_des">规格4+32G 颜色：巴黎蓝</view>
								<view class="right_count">库存紧张</view>
								<view class="right_price">￥118</view>
								<image class="right_delete" src="/static/delete.png" ></image>
							</view>
						</view>
					</view>
					<view class="empty" style="display: none;">
						<image class="empty_img" src="/static/person_empty.png" ></image>
						<view class="empty_txt">暂无收藏哦，快去逛逛吧～</view>
					</view>
				</view>
			</view>
			<view v-show="current === 1">
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
			<view v-show="current === 2">
				<view class="book">
					<view class="book_left">
						<view class="left_title">
							在校园如何潜移默化做推广销售
						</view>
						<view class="left_bottom">
							<text class="bottom_name">中微直供</text>
							<text class="bottom_date">2019-01-23</text>
							<image class="bottom_icon" src="/static/collect1a.png" ></image>
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
							<text class="bottom_name">中微直供</text>
							<text class="bottom_date">2019-01-23</text>
							<image class="bottom_icon" src="/static/collect1.png" ></image>
							<text class="bottom_num">128</text>
						</view>
					</view>
					<view class="book_right">
						<image class="right_img" src="" ></image>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import uniSegmentedControl from '../../components/uni-segmented-order.vue';
	export default {
		data() {
			return {
				items: [
					'商品',
					'卖货素材',
					'成功笔记',
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
.collect{
    .list{
		background: #fff;
        .item{
            overflow: hidden;
            border-bottom:1upx solid #f2f2f2;
            padding:26upx 40upx 39upx 82upx;
            .item_left{
                float: left;
                .left_img{
                    width: 180upx;
                    height: 180upx;
                    background:#8E8E93;
                }     
            }
            .item_right{
                float: left;
                width: 426upx;
                margin-left:12upx;
                position: relative;
                .right_title{
                    font-size: 26upx;
                    line-height: 26upx;
                    color: rgb(51, 51, 51);
                }
                .right_des{
                    font-size: 24upx;
                    line-height: 24upx;
                    color: rgb(153, 153, 153);  
                    margin-top:20upx;
                    margin-bottom:32upx;
                }
                .right_count{
                    font-size: 24upx;
                    line-height: 24upx;
                    color:rgb(255, 0, 13);
                    margin-bottom:26upx;
                }
                .right_price{
                    font-size: 30upx;
                    line-height: 30upx;
                    color:rgb(255, 0, 13);
                }
                .right_delete{

                    position: absolute;
                    bottom:6upx;
                    right:0;
                    width:34upx;
                    height: 36upx;
                }
            }
        }     
    }
    .empty{
        position: relative;
        .empty_img{
            position: absolute;
            top:322upx;
            left:51upx;
            width:648upx;
            height: 468upx;
        }    
        .empty_txt{
            position: absolute;
            top:796upx;
            left:0;
            width:750upx;
            text-align: center;
            font-size: 26upx;
            color:rgb(153, 153, 153);
        }
    }
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
				vertical-align: middle;
			}
			.bottom_date{
				font-size:22upx;
				line-height:22upx;
				color:#666;
				vertical-align: middle;
			}
			.bottom_icon{
				width:36upx;
				height:32upx;
				margin-right:6upx;
				margin-left:60upx;
				vertical-align: middle;
			}
			.bottom_num{
				font-size:22upx;
				line-height:22upx;
				color:#333;
				vertical-align: middle;
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
}
</style>
