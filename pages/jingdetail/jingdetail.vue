<template>
	<view>
		<view>
			<uni-segmented-control 
				:current="current" 
				:values="items" 
				styleType="text"
				v-on:clickItem="onClickItem" >
			</uni-segmented-control>
		</view>
		<view class="container">
			<view v-show="current === 0">
				<view class="content">
					<swiper
						class="slide_swiper"
				
						:autoplay="autoplay"
						:interval="interval"
						:duration="duration">
						<swiper-item>
							<view class="info">
								<view class="collect">
									<uni-icon size="16" type="star" color="#fff"></uni-icon>
									<text class="collect_txt">收藏</text>
								</view>
								<view class="page">3/3</view>
							</view>
						</swiper-item>
						<swiper-item>
							<view class="info">
								<view class="collect">
									<uni-icon size="16" type="star" color="#fff"></uni-icon>
									<text class="collect_txt">收藏</text>
								</view>
								<view class="page">3/3</view>
							</view>
						</swiper-item>
						<swiper-item>
							<view class="info">
								<view class="collect">
									<uni-icon size="16" type="star" color="#fff"></uni-icon>
									<text class="collect_txt">收藏</text>
								</view>
								<view class="page">3/3</view>
							</view>
						</swiper-item>
					</swiper>
					<view class="des">
						<view class="price">
							<text class="current">￥118</text>
							<text class="origin">￥118</text>
						</view>
						<view class="post">满100免邮费</view>
						<view class="title">网红便携式手持电熨斗</view>
					</view>
					<view class="send">
						<image class="send_img" src="/static/post_cart.png"></image>
						<text class="send_txt">48小时发货</text>
					</view>
					<view class="shop">
						<image class="shop_label"></image>
						<view class="shop_value">中微直供官方旗舰店</view>
						<image class="shop_icon" src="/static/my.png"></image>
					</view>
					<view class="gui" @click="showGuiPopup">
						<view class="gui_label">规格</view>
						<view class="gui_value">选择 颜色分类 款式</view>
						<image class="gui_icon" src="/static/my.png"></image>
					</view>
					<view class="address">
						<view class="address_label">地址</view>
						<view class="address_value">选择收货地址</view>
						<image class="address_icon" src="/static/my.png"></image>
					</view>
					<view class="bottom_bar">
						<detail-bar></detail-bar>
					</view>
				</view>
			</view>
			<view v-show="current === 1" style="background: #fff;">
				<view class="discuss_tab">
					<uni-button-control 
						:current="ccurrent" 
						:values="citems" 
						v-on:clickItem="onClickCItem" >
					</uni-button-control>
				</view>
				<view v-show="ccurrent === 0">
					<view class="discuss">
						<view class="header">
							<view class="header_label">商品评价(257)</view>
							<image class="header_icon" src="/images/static/my.png"></image>
							<view class="header_value">查看全部</view>
						</view>
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
							<view class="item_date">2019.01.27 颜色：蓝色 500ml</view>
						</view>
					</view>
				</view>
				<view v-show="ccurrent === 1">
					ffffff
				</view>
				<view v-show="ccurrent === 2">
					ffff
				</view>
			</view>
			<view v-show="current === 2">
				<view class="goods">
					<view class="goods_title">商品详情</view>
					<image class="goods_img"></image>
					<image class="goods_img"></image>
				</view>
			</view>
		</view>

		<view class="attr">
			<uni-popup :show="showPopupGui" type="bottom" v-on:hidePopup="hidePopup">
				<view class="popup_attr">
					<view class="back">
						<image class="img"></image>
						<view class="attr_top">
							<view class="top_right">
								<image class="right_close" src="/static/close.png" @click="hidePopup"></image>
							</view>
							<view class="top_middle">
								<view class="des_price">￥118</view>
								<view class="des_count">库存9971</view>
								<view class="des_select">已选择："150ml"</view>
							</view>
						</view>
					</view>
					<view class="attr_gui">
						<view class="gui_title">规格</view>
						<view class="gui_list">
							<view class="gui_item gactive">100ml</view>
							<view class="gui_item">150ml</view>
						</view>
					</view>
					<view class="attr_color">
						<view class="color_title">颜色分类</view>
						<view class="color_list">
							<view class="color_item cactive">
								<image class="item_img" src=""></image>
								<text class="item_txt">100ml</text>
							</view>
							<view class="color_item">
								<image class="item_img" src=""></image>
								<text class="item_txt">100ml</text>
							</view>
						</view>
					</view>
					<view class="num">
						<view class="num_left">购买数量</view>
						<view class="num_right">
							<uni-number-box></uni-number-box>
						</view>
					</view>
					<view class="bottomss">
						<view class="bottomss_cart">加入购物车</view>
						<view class="bottomss_buy">确定</view>
					</view> 
				</view>
			</uni-popup>
		</view>
	</view>
</template>

<script>
	import uniSegmentedControl from '../../components/uni-segmented-order.vue';
	import uniButtonControl from '../../components/uni-button-control.vue';
	import uniPopup from '../../components/uni-popup.vue';
	import detailBar from '../../components/detail-bar.vue';
	import uniNumberBox from '../../components/uni-number-box.vue'
	export default {
		components: {
			uniSegmentedControl,
			uniPopup,
			uniButtonControl,
			detailBar,
			uniNumberBox,
		},
		data() {
			return {
				items: [
					'商品',
					'评价',
					'详情',
				],
				citems: [
					'全部（1044）',
					'追加（441）',
					'有图（2357）',
					'质量很好（105344）'
				],
				current: 0,
				ccurrent: 0,
				indicatorDots: true,
				autoplay: true,
				interval: 5000,
				duration: 1000,
				showPopupGui:false,
			}
		},
		methods: {
			onClickItem(index) {
				if (this.current !== index) {
					this.current = index;
				}
			},
			onClickCItem(index) {
				if (this.ccurrent !== index) {
					this.ccurrent = index;
				}
			},
			hidePopup:function(){
				this.showPopupGui=false;
			},
			showGuiPopup:function(){
				console.log("ddd");
				this.hidePopup();
				this.showPopupGui=true;
			}
		}
	}
</script>

<style lang="scss">
	page {
		height: auto;
		background-color:#f7f7f7;
		margin-bottom:100upx;
	}
	.container {
		.content{
            .slide_swiper{
                width: 750upx;
                height: 734upx; 
                .info{
                	text-align: right;
                	margin-top: 650upx;
                	vertical-align: middle;
                	.collect{
                		display: inline;
                		margin-right: 20upx;
                		border-radius: 30upx;
                		padding:10upx 16upx;
                		background: rgba($color: #000000, $alpha: .3);
                		.collect_txt{
                			font-size: 24upx;
                			line-height: 24upx;
                			color: #fff;
                		}
                	}
                	.page{
                		display: inline;
                		margin-right: 50upx;
                		border-radius: 30upx;
                		padding:12upx 30upx;
                		background: rgba($color: #000000, $alpha: .3);
                		font-size: 24upx;
                		line-height: 24upx;
                		color: #fff;
                	}
                }
            }
            .des{
                padding:40upx 22upx 30upx 22upx;
                background: #fff;
                .price{
                   font-size: 30upx;
                   line-height: 30upx;
                    .current{
                        color:rgb(255, 0, 13);
                    }
                    .origin{
                        text-decoration: line-through;
                        color:rgb(152,152,152);
                        margin-left:12upx;
                    }
                }
                .post{
                    width:142upx; 
                    height: 28upx;
                    font-size: 22upx;
                    line-height: 26upx;
                    text-align: center;
                    border:3upx solid rgb(255, 0, 13);
                    color:rgb(255, 0, 13);
                    border-radius: 4upx;
                    margin-top:36upx;
                }
                .title{
                    font-size: 36upx;
                    line-height: 36upx;
                    margin-top:26upx;
                    color:rgb(40, 40, 40);
                }
            }
            .send{
                overflow: hidden;
                padding:30upx 22upx;
                background: #fff;
                border-top: 1upx solid #f2f2f2;
                border-bottom: 1upx solid #f2f2f2;
                .send_img{
                    float: left;
                    width: 34upx;
                    height: 34upx;
                    border-radius: 50%;
                }
                .send_txt{
                    float: left;
                    font-size: 30upx;
                    line-height: 30upx;
                    color: rgb(152,152,152);
                    margin-left:20upx;
                    margin-top:4upx;
                }
            }
            .shop{
                overflow: hidden;
                background:#fff;
                padding:35upx 22upx;
                margin-bottom:16upx;
                .shop_label{
                    float: left;
                    width: 58upx;
                    height: 58upx;
                    border-radius: 50%;
                    background: #333;
               } 
               .shop_value{
                    float: left;
                    font-size: 30upx;
                    line-height: 30upx;
                    color:rgb(51, 51, 51);
                    margin-left: 25upx;
                    margin-top:18upx;
               }
               .shop_icon{
                    float: right;
                    width: 16upx;
                    height: 27upx;
                    margin-left: 20upx;
                    margin-top:18upx;
               }
            }
            .gui{
                overflow: hidden;
                background:#fff;
                padding:30upx 22upx;
                border-bottom: 1upx solid #f2f2f2;
               .gui_label{
                    float: left;
                    font-size: 30upx;
                    line-height: 30upx;
                    color:#666;
               } 
               .gui_value{
                    float: left;
                    font-size: 30upx;
                    line-height: 30upx;
                    color:rgb(51, 51, 51);
                    margin-left: 45upx;
               }
               .gui_icon{
                    float: right;
                    width: 16upx;
                    height: 27upx;
                    margin-left: 20upx;
               }
            }
            .address{
                overflow: hidden;
                background:#fff;
                padding:30upx 22upx;
                margin-bottom: 16upx;
                .address_label{
                    float: left;
                    font-size: 30upx;
                    line-height: 30upx;
                    color:#666;
                } 
                .address_value{
                    float: left;
                    font-size: 30upx;
                    line-height: 30upx;
                    color:rgb(51, 51, 51);
                    margin-left: 45upx;
                }
                .address_icon{
                    float: right;
                    width: 16upx;
                    height: 27upx;
                    margin-left: 20upx;
                }
            }
            .discuss{
                .header{
                    overflow: hidden;
                    background:#fff;
                    padding:30upx 22upx;
                   .header_label{
                        float: left;
                        font-size: 30upx;
                        line-height: 30upx;
                        color:rgb(40, 40, 40);
                   } 
                   .header_value{
                        float: right;
                        font-size: 30upx;
                        line-height: 30upx;
                        color:rgb(102, 102, 102);
                   }
                   .header_icon{
                        float: right;
                        width: 16upx;
                        height: 27upx;
                        margin-left: 20upx;
                   }
                }
                .item{
                    .item_header{
                        margin-top:16upx;
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
                    .item_date{
                        background: #fff;
                        padding:18upx 19upx 26upx 19upx;
                        font-size: 24upx;
                        line-height: 24upx;
                        color: rgb(51, 51, 51);
                    }
                }
            }
            .bottom_bar{
                .van-info {
                    right:3upx;
                    top:-6px;
                }   
            }
        }
        .discuss{
			.header{
				overflow: hidden;
				background:#fff;
				padding:30upx 22upx;
			   .header_label{
					float: left;
					font-size: 30upx;
					line-height: 30upx;
					color:rgb(40, 40, 40);
			   } 
			   .header_value{
					float: right;
					font-size: 30upx;
					line-height: 30upx;
					color:rgb(102, 102, 102);
			   }
			   .header_icon{
					float: right;
					width: 16upx;
					height: 27upx;
					margin-left: 20upx;
			   }
			}
			.item{
				.item_header{
					margin-top:16upx;
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
				.item_date{
					background: #fff;
					padding:18upx 19upx 26upx 19upx;
					font-size: 24upx;
					line-height: 24upx;
					color: rgb(51, 51, 51);
				}
			}
		}
		.goods{
		    .goods_title{
		        background: #fff;
		        height: 66upx;
		        font-size: 30upx;
		        line-height:66upx;
		        padding-left:20upx;
		    }    
		    .goods_img{
		        width: 750upx;
		        height: 500upx;
		        background: #333;
		        vertical-align: bottom;
		    }
		}
	}
	.attr{
		.popup_attr{
			.back{
				position: relative;
				height: 268upx;
				.img{
					z-index: 100;
					position: absolute;
					top:0upx;
					left:16upx;
					width: 240upx;
					height: 240upx;
					background: red;
					border-radius: 10upx;
				}
				.attr_top{
					z-index: 1;
					position: absolute;
					top:80upx;
					left:0upx;
					padding-top:40upx;
					padding-bottom:45upx;
					background: #fff;
					width: 750upx;
					height: 106upx;
					.top_middle{
						float:left;
						margin-left:290upx;
						.des_price{
							font-size: 30upx;
							line-height: 30upx;
							color: #FF000D;
						}
						.des_count{
							font-size: 24upx;
							line-height: 24upx;
							color:#666;
							margin-top:18upx;
							margin-bottom:16upx;
						}
						.des_select{
							font-size: 22upx;
							line-height: 22upx;
							color:#333;
						}
					}
					.top_right{
						float: right;
						margin-right: 36upx;
						.right_close{
							width: 40upx;
							height: 40upx;
						}
					}
				}
			}
			.attr_gui{
				background: #fff;
				padding:22upx 34upx 18upx 34upx;
				.gui_title{
					font-size: 24upx;
					line-height: 24upx;
					margin-bottom: 20upx;
				}
				.gui_list{
					overflow: hidden;
					.gui_item{
						float: left;
						width:164upx;
						height: 58upx;
						line-height: 58upx;
						text-align: center;
						color:#333;
						font-size: 20upx;
						background: #F2F2F2;
						border-radius: 6upx;
						margin-left:20upx;
					}
					.gactive{
						border:1upx solid #FF000D;
						color:#FF000D;
						background: transparent;
					}
				}
			}
			.attr_color{
				background: #fff;
				padding:22upx 34upx 18upx 34upx;
				border-top: 1upx solid #f2f2f2;
				.color_title{
					font-size: 24upx;
					line-height: 24upx;
					margin-bottom: 20upx;
				}
				.color_list{
					overflow: hidden;
					.color_item{
						float: left;
						width:164upx;
						height: 58upx;
						line-height: 58upx;
						text-align: center;
						color:#333;
						font-size: 20upx;
						background: #F2F2F2;
						border-radius: 6upx;
						margin-left:20upx;
						overflow: hidden;
						.item_img{
							margin-top:6upx;
							margin-left: 8upx;
							float: left;
							width: 66upx;
							height: 46upx;
							background: #666;
						}
						.item_txt{
							float: left;
							font-size: 24upx;
							line-height: 24upx;
							margin-left: 12upx;
							margin-top:18upx;
						}
					}
					.cactive{
						border:1upx solid #FF000D;
						color:#FF000D;
						background: transparent;
					}
				}
			}
			.num{
				padding:60upx 20upx 228upx 34upx;
				background: #fff;
				border-top: 1upx solid #f2f2f2;
				height:60upx;
				.num_left{
					float: left;
					font-size: 24upx;
					line-height: 24upx;
					margin-top:20upx;
				}
				.num_right{
					float: right;
				}
			}
			.bottomss{
				width: 750upx;
				height: 100upx;
				font-size: 24upx;
				line-height: 100upx;
				text-align: center;
				overflow: hidden;
				border-top: 1upx solid #f2f2f2;
				.bottomss_cart{
					float: left;
					width: 375upx;
					height: 100upx;
					line-height: 100upx;
					background: #fff;
				}
				.bottomss_buy{
					float: left;
					width: 375upx;
					background: #D41C1C;
					height: 100upx;
					line-height: 100upx;
					color:#fff;
				}
			}
		}
	}
	.popup_ping {
		width: 612rpx;
		height: 500rpx;
		border-radius: 30upx;
		background: #fff;
		margin: 0 auto;
	
		.ping_delete {
			text-align: right;
			padding-top: 28rpx;
			padding-right: 34rpx;
		}
	
		.ping_title {
			overflow: hidden;
			font-size: 30rpx;
			line-height: 30rpx;
			color: #333;
			text-align: center;
		}
	
		.ping_des {
			margin-top: 28rpx;
			font-size: 24rpx;
			line-height: 24rpx;
			color: #666666;
			text-align: center;
		}
	
		.ping_img {
			margin-top: 52rpx;
	
			.img1 {
				margin-left: 186rpx;
				width: 94rpx;
				height: 94rpx;
			}
	
			.img2 {
				margin-left: 82rpx;
				width: 94rpx;
				height: 94rpx;
			}
		}
	
		.ping_btn {
			width: 430rpx;
			height: 64rpx;
			margin: 0 auto;
			border-radius: 10rpx;
			font-size: 28rpx;
			line-height: 64rpx;
			text-align: center;
			margin-top: 64rpx;
			background: #FFD944;
		}
	
	}
	
	.popup_can {
		width: 578rpx;
		height: 772rpx;
		background: #fff;
		margin: 0 auto;
		position: relative;
	
		.can_title {
			padding: 37rpx 0;
			font-size: 30rpx;
			line-height: 30rpx;
			text-align: center;
			color: #333;
			border-bottom: 1rpx solid #f2f2f2;
		}
	
		.can_delete {
			position: absolute;
			top: 25rpx;
			right: 20rpx;
		}
	
		.can_item {
			overflow: hidden;
			border-bottom: 1rpx solid #f2f2f2;
	
			.item_left {
				float: left;
				margin-top: 28rpx;
				margin-left: 26rpx;
	
				.left_img {
					width: 74rpx;
					height: 74rpx;
				}
			}
	
			.item_middle {
				float: left;
				margin-left: 17rpx;
	
				.middle_top {
					margin-top: 30rpx;
					font-size: 26rpx;
					line-height: 26rpx;
					color: #333;
	
					.top_num {
						margin-left: 15rpx;
						color: #666;
					}
				}
	
				.middle_bottom {
					margin-top: 18rpx;
					font-size: 26rpx;
					line-height: 26rpx;
					color: #999;
				}
			}
	
			.item_right {
				float: right;
				margin-top: 33rpx;
				margin-right: 20rpx;
				width: 138rpx;
				height: 62rpx;
				line-height: 62rpx;
				text-align: center;
				font-size: 26rpx;
				color: #fff;
				background: #D41C1C;
				border-radius: 10rpx;
	
			}
	
		}
	}
</style>

