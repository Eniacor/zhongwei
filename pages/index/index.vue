<template>
	<view>
		<view class="back">
			<view class="banner">
				<swiper
					class="slide_swiper"
					:indicator-dots="indicatorDots"
					:autoplay="autoplay"
					:interval="interval"
					:duration="duration">
					<swiper-item>
						<image src="" class="slide_image" width="355" height="150" />
					</swiper-item>
					<swiper-item>
						<image src="" class="slide_image" width="355" height="150" />
					</swiper-item>
					<swiper-item>
						<image src="" class="slide_image" width="355" height="150" />
					</swiper-item>
				</swiper>
			</view>
			<view class="location">
				<image class="location_left"></image>
				<view class="location_right" v-if="search">
					<view class="right_school">
						<view class="school_title">南京艺术学院</view>
						<view class="school_des">Alex为您推荐</view>
					</view>
					<view class="right_search" @click="onPopupSearch">
						<image class="search_img" src="/static/search.png"></image>
						<text class="search_txt">商品</text>
					</view>
					<image class="right_intro" src="/static/intro.png"  @click="showInfoPopup"></image>
					<image class="right_msg" src="/static/icode.png"    @click="showCodePopup"></image>
				</view>
				<view class="location_right_search" v-if="!search">
					<view class="search_btn">
						<image class="btn_img" src="/static/search.png"></image>
					</view>
					<view class="search_input" >
						<input class="input" placeholder="搜索你感兴趣的商品" auto-focus />
						<view class="img" @click="onPopupSearch">
							<image class="img_p"src="/static/clear.png"></image>
						</view>
					</view>
				</view>
			</view>
		</view> 
		<view style="margin-left:13upx;">
			<uni-segmented-control 
				:current="current" 
				:values="items" 
				v-on:clickItem="onClickItem" >
			</uni-segmented-control>
		</view>
		<view class="content">
			<view v-show="current === 0">
				<view class="first">
					<view class="header">
					  <image class="top_img" src="/static/ping.png"></image>
					  <text class="top_txt1">同校拼单</text>
					  <text class="top_txt2">(暂未开通跨校区拼单业务哦～)</text>
					</view>
					<navigator hover-class="none" url="/pages/pindetail/pindetail">
					<view class="item">
						<view class="item_left">
						  <image class="left_img" src=""></image>
						</view>
						<view class="item_right">
						  <view class="right_top">[宿舍必备神器] 大功率电器转换插排</view>
						  <view class="right_middle">包邮</view>
						  <view class="right_tuan1">
							<text class="tuan1_num">2人团</text>
							<text class="tuan1_price">￥29.9</text>
							<text class="tuan1_origin">69.9</text>
						  </view>
						  <view class="right_tuan2">
							<text class="tuan2_txt">开团倒计时：</text>
							<text class="tuan2_time">2天 23:14:10</text>
						  </view>
						  <view class="right_btn">立即拼单</view>
						</view>
					</view>
					</navigator>
					<view class="item margin16">
						<view class="item_left">
							<image class="left_img" src=""></image>
						</view>
						<view class="item_right">
							<view class="right_top">[宿舍必备神器] 大功率电器转换插排</view>
							<view class="right_middle">包邮</view>
							<view class="right_tuan1">
								<text class="tuan1_num">2人团</text>
								<text class="tuan1_price">￥29.9</text>
								<text class="tuan1_origin">69.9</text>
							</view>
							<view class="right_tuan2">
							  <text class="tuan2_txt">开团倒计时：</text>
							  <text class="tuan2_time">2天 23:14:10</text>
							</view>
							<view class="right_btn">立即拼单</view>
						</view>
					</view>
				</view>
				<view class="second">
					<view class="header">
						<image class="top_img" src="/static/gift.png"></image>
						<text class="top_txt1">开学大礼包</text>
						<text class="top_txt2">感恩开学季，优惠大放送</text>
					</view>
					<navigator hover-class="none" url="/pages/giftdetail/giftdetail">
						<view class="item">
							<view class="item_top">
								<image class="left_img" src=""></image>
							</view>
							<view class="item_bottom">
								<view class="bottom_title">良品铺子坚果大礼包1339g年货礼盒</view>
								<view class="bottom_des">良品铺子坚果大礼包1339g年货礼盒</view>
								<view class="bottom_price">
									<text class="price_account">￥118</text>
									<text class="price_orign">￥158</text>
								</view>
								<view class="bottom_btn">查看详情</view>
							</view>
						</view>
					</navigator>
					<view class="item margin16">
						<view class="item_top">
							<image class="left_img" src=""></image>
						</view>
						<view class="item_bottom">
							<view class="bottom_title">良品铺子坚果大礼包1339g年货礼盒</view>
							<view class="bottom_des">良品铺子坚果大礼包1339g年货礼盒</view>
							<view class="bottom_price">
								<text class="price_account">￥118</text>
								<text class="price_orign">￥158</text>
							</view>
							<view class="bottom_btn">查看详情</view>
						</view>
					</view>
				</view>
				<view class="three">
					<view class="header">
						<image class="top_img" src="/static/get.png"></image>
						<text class="top_txt1">精选好物</text>
						<text class="top_txt2">感恩开学季，优惠大放送</text>
					</view>
					<navigator hover-class="none" url="/pages/jingdetail/jingdetail">
						<view class="item">
							<view class="item_left">
								<image class="left_img" src=""></image>
							</view>
							<view class="item_right">
								<view class="right_top">Semir 拼接链条单肩包</view>
								<view class="right_des">糖果配色 十足少女心</view>
								<view class="right_middle">包邮</view>
								<view class="right_price">￥118.9</view>
								<view class="right_account">已售395件</view>
								<view class="right_btn">立即购买</view>
							</view>
						</view>
					</navigator>
					<view class="item margin16">
						<view class="item_left">
							<image class="left_img" src=""></image>
						</view>
						<view class="item_right">
							<view class="right_top">Semir 拼接链条单肩包</view>
							<view class="right_des">糖果配色 十足少女心</view>
							<view class="right_middle">包邮</view>
							<view class="right_price">￥118.9</view>
							<view class="right_account">已售395件</view>
							<view class="right_btn">立即购买</view>
						</view>
					</view>
				</view>
			</view>
			<view v-show="current === 1">
				电器
			</view>
			<view v-show="current === 2">
				宿舍
			</view>
			<view v-show="current === 3">
				数码3
			</view>
			<view v-show="current === 4">
				美妆
			</view>
		</view>
		<!--code -->
		<view class="code">
			<uni-popup :show="showPopupCode" type="middle" v-on:hidePopup="hidePopup">
				<view class="popup_code">
					<image class="code_ma" src=""></image>
					<image class="code_delete" src="../../static/close.png"></image>
					<view class="code_title">长按保存二维码，使用微信</view>
					<view class="code_title">添加代理商</view>
				</view>
			</uni-popup>
		</view>
		<view class="info">
			<!--info -->
			<uni-popup :show="showPopupInfo" type="middle" v-on:hidePopup="hidePopup">
				<view class="popup_content">
					<view class="content_header" >
						<image src="/static/close.png" class="close"  @click="hidePopup"></image>
					</view>
					<view class="content_title">
					  <image class="title_right"></image>
					  <view class="title_left">Alex</view>
					</view>
					<view class="content_des">
					  本店带来了的肯定打开快点快点
					  本店带来了的肯定打开快点快
					  开快点快点看看看看多看看打开看看端口打开看到看到
					</view>
					<view class="content_address">
					  <view class="address_name">店铺名称：南京艺术学院</view>
					  <view class="address_tel">联系方式：18360172424</view>
					  <view class="address_area">销售区域：江苏省南京事鼓楼区</view>
					</view>
				  </view>
			</uni-popup>
		</view>
	</view>
</template>

<script>
	import uniSegmentedControl from '../../components/uni-segmented-index.vue';
	import uniPopup from '../../components/uni-popup.vue';
	export default {
		data() {
			return {
				items: [
					'推荐',
					'电器',
					'宿舍',
					'数码3C',
					'美妆',
				],
				current: 0,
				intro:false,  //是否显示介绍
				code:false,   //是否显示二维码
				search:true   ,//是否显示搜索框
				indicatorDots: true,
				autoplay: true,
				interval: 5000,
				duration: 1000,
			
				showPopupCode: false,
				showPopupInfo: false,
			}
		},
		components: {
			uniSegmentedControl,
			uniPopup
		},
		methods: {
			onClickItem(index) {
				if (this.current !== index) {
					this.current = index;
				}
			},
// 			//弹出介绍信息
// 			onPopupIntro:function(e){
// 				this.setData({
// 				  intro:!this.data.intro,
// 				});
// 			 },
			//弹出/关闭搜索信息
			onPopupSearch:function(){
				this.search=!this.search;
				console.log(this.search);
			},
// 			//弹出/关闭二维码信息
// 			onPopupCode:function(e){
// 				this.setData({
// 				  code:!this.data.code,
// 				});
// 			},
			//统一的关闭popup方法
			hidePopup: function() {
				this.showPopupCode = false;
				this.showPopupInfo = false;
			},
			//展示居中 popup
			showCodePopup: function() {
				this.hidePopup();
				this.showPopupCode = true;
			},
			//展示居中 popup
			showInfoPopup: function() {
				this.hidePopup();
				this.showPopupInfo = true;
			},
		}
	}
</script>

<style lang="scss">
	page {
		height: auto;
		background-color:#f7f7f7;
	}
	
	.back{
        position: relative;
        width: 750upx;
        height: 432upx;
        background: linear-gradient(#FFD944, #F2F2EF);
        margin-bottom:40upx;
        .banner{
            position: absolute;
            top:0;
            left:13upx;
            .slide_swiper{
                width: 724upx;
                height: 306upx;
                border-radius: 10upx;
                .slide_image{
                    width: 724upx;
                    height: 306upx;
                    border-radius: 10upx;
                    background: #333;
                } 
            }
        }
        .location{
            position: absolute;
            top:326upx;
            left:13upx;
            overflow: hidden;
            width: 724upx;
            height: 134upx;
            background: #fff;
            margin:0 auto;
            border-radius: 10upx;
            .location_left{
                float: left;
                width: 94upx;
                height: 94upx;
                background: #333;
                border-radius: 50%;
                margin-top:13upx;
                margin-left: 13upx;
                margin-right: 27upx;
            }
            .location_right{
                float: left;
                width: 590upx;
                .right_school{
                    float: left;
                    .school_title{
                        margin-top:29upx;
                        font-size: 30upx;
                        line-height: 30upx;
                        color: rgb(40,40,40);
                    }  
                    .school_des{
                        margin-top:11upx;
                        font-size: 24upx;
                        line-height: 24upx;
                        color: #999;
                    }
                }
                .right_msg{
                    float: right;
                    width:48upx;
                    height: 48upx;
                    margin-top:38upx;
                    margin-right:34upx;
                }
                .right_intro{
                    float:right;
                    margin-top:36upx;
                    margin-right:56upx;
                    width:40upx;
                    height:48upx;
                }
                .right_search{
                    float: right;
                    width: 150upx;
                    height: 60upx;
                    border-radius: 30upx;
                    border:1upx solid #f2f2f2;
                    line-height: 60upx;
                    margin-top:32upx;
                    margin-right:12upx;
                    .search_img{
                        float: left;
                        margin-top:19upx;
                        margin-left:25upx;
                        margin-right:24upx;
                        width: 24upx;
                        height: 23upx;
                        vertical-align: bottom;
                    }
                    .search_txt{
                        float: left;
                        font-size: 24upx;
                        color:#999;
                    }
                }
            }
            .location_right_search{
                width: 542upx;
                float: right;
                padding-top:33upx;
                padding-right:48upx;
                .search_btn{
                    float: right;
                    width: 96upx;
                    height: 60upx;
                    border-radius: 30upx;
                    border:1upx solid #f2f2f2;
                    .btn_img{
                        width:24upx;
                        height: 23upx; 
                        margin-left:36upx;
                        margin-top:20upx;
                    }
                }
                .search_input{
                    float: right;
                    width: 400upx;
                    height: 60upx;
                    position: relative;
                    border-radius: 30upx;
                    box-shadow:0upx 0upx 20upx #F0F0F0;
                    margin-right: 20upx;
                    .input{
                        width: 400upx;
                        height: 60upx;
                        font-size: 24upx;
                        color:rgb(102, 102, 102);
                        padding-left:36upx;
                    }
                    .img{
                        position: absolute;
                        top:13upx;
                        right:20upx;
                        width: 34upx;
                        height: 34upx;
                        z-index: 100;
						.img_p{
							width: 34upx;
							height: 34upx;
							display:block;
						}
                    }
                }
            }
            
        }
    }
// 	.uni-padding-wrap{
// 		margin-left: 13upx;
// 	}
	.content {
		width: 724upx;
        margin: 0 auto;
		margin-top: 16upx!important;
		.first{
            width: 100%;
			.header{
                width: 100%;
                height: 32upx;
                background: #fff;
                overflow: hidden;
                border-top-left-radius: 10upx;
                border-top-right-radius: 10upx;
				padding:54upx 0 46upx 0;
                display: flex;
				flex-direction: row;
                align-items: center;
                justify-content: start; 
                .top_img{
					float: left;
                    width:32upx;
                    height:32upx;
                    margin-left:34upx;
                }
				.top_txt1{
					font-size: 32upx;
					line-height: 32upx;
					margin:0 16upx 0 13upx;
					color:#4D4D4D;
                }
				.top_txt2{
					font-size: 24upx;
					line-height: 24upx;
					color:#989898;
				}
			}
			.item{
				padding-top:23upx;
				padding-left:11upx;
				padding-bottom:29upx;
				background: #fff;
				overflow: hidden;
				.item_left{
					float: left;
					width: 241upx;
					.left_img{
					   width: 241upx;
					   height: 259upx; 
						background: #989898;
					}
				}
				.item_right{
					float: left;
					width: 452upx;
					margin-left:20upx;
					position: relative;
					.right_top{
						width: 100%;
						height:60upx;
						font-size: 28upx;
						line-height: 32upx;
						color:#4D4D4D;
					}
					.right_middle{
						width: 82upx;
						height: 26upx;
						line-height: 26upx;
						text-align: center;
						color:#fff;
						font-size: 20upx;
						background-color: #FFD944;
						border-radius: 50upx;
						margin-top:20upx;
						margin-bottom:43upx;
					}
					.right_tuan1{
						line-height: 24upx;
						.tuan1_num{
							font-size: 24upx;
							color: #333;
						}
						.tuan1_price{
							font-size: 24upx;
							color: #333;
							margin-left:17upx; 
							margin-right: 10upx;
						}
						.tuan1_origin{
							font-size: 18upx;
							color: #333;
							text-decoration:line-through;
						}
					}
					.right_tuan2{
						margin-top:13upx;
						line-height: 20upx;
						.tuan2_txt{
							font-size: 20upx;
							color: rgb(51, 51, 51);
						} 
						.tuan2_time{
							font-size: 20upx;
							color: #FF1924;
						}
					}
					.right_btn{
						position: absolute;
						top:177upx;
						right:0;
						width: 144upx;
						height: 52upx;
						line-height:52upx;
						text-align: center; 
						border-top-left-radius: 24upx;
						border-bottom-left-radius:24upx; 
						background: #FF000D;
						color:#fff;
						font-size: 28upx;
					}
				}
			}
			.margin16{
				margin-top: 16upx;
			}
		}
		.second{
			width: 100%;
			margin-top: 16upx;
			.header{
				width: 100%;
				height: 32upx;
				background: #fff;
				overflow: hidden;
				border-top-left-radius: 10upx;
				border-top-right-radius: 10upx;
				padding:54upx 0 46upx 0;
				display: flex;
				flex-direction: row;
				align-items: center;
				justify-content: start; 
				.top_img{
					float: left;
					width: 32upx;
					height: 32upx;
					margin-left:34upx;
				}
				.top_txt1{
					font-size: 32upx;
					line-height: 32upx;
					margin:0 16upx 0 13upx;
					color:#4D4D4D;
				   
				}
				.top_txt2{
					font-size: 24upx;
					line-height: 24upx;
					color:#989898;

				}

			}
			.item{
				background: #fff;
				position: relative;
				.item_top{
					.left_img{
						width:724upx;
						height: 299upx;
						border-radius: 10upx;
						background: #989898;
						vertical-align: bottom;
					}
				}
				.item_bottom{
					// height: 67upx;
					padding-top:24upx;
					padding-bottom: 27upx;
					padding-left:20upx;
					.bottom_title{
						font-size: 30upx;
						line-height: 30upx;
						color:rgb(40,40,40);
					}
					.bottom_des{
						font-size: 24upx;
						line-height: 24upx;
						color:rgb(40,40,40);
						margin-top:13upx;
					}
					.bottom_price{
						margin-top:42upx;
						font-size: 36upx;
						line-height: 36upx;
						.price_account{
							color:rgb(255,0,13);
						}
						.price_orign{
							margin-left: 11upx;
							color:#999999;
							text-decoration:line-through;
						}
					}
					.bottom_btn{
						position: absolute;
						top:410upx;
						right: 8upx;
						width: 130upx;
						height: 58upx;
						line-height: 58upx;
						text-align: center;
						border-radius: 10upx;
						font-size: 24upx;
						color:#fff;
						background: rgb(255,0,13);
					}
				}
			}
			.margin16{
				margin-top: 16upx;
			}
		}
		.three{
			margin-top: 16upx;
			width: 100%;
			.header{
				width: 100%;
				height: 32upx;
				background: #fff;
				overflow: hidden;
				border-top-left-radius: 10upx;
				border-top-right-radius: 10upx;
				padding:54upx 0 46upx 0;
				display: flex;
				flex-direction: row;
				align-items: center;
				justify-content: start; 
				.top_img{
					float: left;
					width: 32upx;
					height: 32upx;
					margin-left:34upx;
				}
				.top_txt1{
					font-size: 32upx;
					line-height: 32upx;
					margin:0 16upx 0 13upx;
					color:#4D4D4D;
				}
				.top_txt2{
					font-size: 24upx;
					line-height: 24upx;
					color:#989898;
				}

			}
			.item{
				padding-top:21upx;
				padding-left:8upx;
				padding-bottom:44upx;
				background: #fff;
				overflow: hidden;
				.item_left{
					float: left;
					.left_img{
						width: 202upx;
						height: 202upx; 
						background: #989898;
					}
				}
				.item_right{
					float: left;
					width: 482upx;
					margin-left:32upx;
					position: relative;
					.right_top{
						width: 100%;
						font-size: 30upx;
						line-height: 30upx;
						color:rgb(51, 51, 51);
					}
					.right_des{
						margin-top:21upx;
						width: 100%;
						font-size: 24upx;
						line-height: 24upx;
						color:rgb(153, 153, 153);
					}
					.right_middle{
						width: 82upx;
						height: 26upx;
						line-height: 26upx;
						text-align: center;
						color:#fff;
						font-size: 20upx;
						background-color: #FFD944;
						border-radius: 6upx;
						margin-top:20upx;
						margin-bottom:47upx;
					}
					.right_price{
						font-size: 30upx;
						line-height: 30upx;
						color: rgb(255, 0, 13);
					}
					.right_account{
						margin-top:34upx;
						font-size: 20upx;
						line-height: 20upx;
						color: rgb(102, 102, 102);
					}
					.right_btn{
						position: absolute;
						top:176upx;
						right:8upx;
						width: 130upx;
						height: 58upx;
						line-height: 58upx;
						text-align: center;
						border-radius: 10upx;
						font-size: 24upx;
						color:#fff;
						background: rgb(255,0,13);
					}
				}
			}
			.margin16{
				margin-top: 16upx;
			}
		}
	}
	.code{
		border-radius: 20upx;
		.popup_code{
			width: 642upx;
			height: 582upx;
			background: #fff;
			position: relative;
			border-radius: 20upx;
			.code_ma{
				width: 242upx;
				height:242upx;
				margin:104upx 200upx 52upx 200upx;
				background: #333;
			}
			.code_delete{
				position: absolute;
				top:16upx;
				right:16upx;
				width:30upx;
				height:30upx;
			}
			.code_title{
				font-size: 38upx;
				line-height: 38upx;
				color:#333;
				text-align: center;
				margin-bottom:16upx;
			}
		}
	}
	.info{
		.popup_content{
			width: 644upx!important;
			height: 580upx!important;
			border-radius:30upx!important;
			background: #fff;
			.content_header{
				text-align:right;
				padding-top:28upx;
				padding-right: 34upx;
				.close{
					width: 34upx;
					height: 34upx;
				}
			}
			.content_title{
				overflow: hidden;
				padding-left:70upx;
				padding-right:40upx;
				.title_left{
					float: left;
					font-size: 36upx;
					line-height: 36upx;
					margin-left:36upx;
					margin-top:34upx;
				}
				.title_right{
					float:left;
					width: 94upx;
					height: 94upx;
					border-radius:50%;
					background:#333;
				}
			}
			.content_des{
				padding-left: 56upx;
				padding-top:54upx;
				width: 456upx;
				font-size: 24upx;
				line-height: 40upx;
			}
			.content_address{
				padding-left: 56upx;
				padding-top:54upx;
				.address_name{
					font-size: 24upx;
					line-height: 24upx;
				}
				.address_tel{
					margin-top:24upx;
					font-size: 24upx;
					line-height: 24upx;
				}
				.address_area{
					margin-top:24upx;
					font-size: 24upx;
					line-height: 24upx;
				}
			}
		}
	}
</style>
