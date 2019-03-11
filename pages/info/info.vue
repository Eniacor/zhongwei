<template>
	<view>
		<view class="person">
			<view class="header">
				<view class="header_top">
					<view class="user_img">
					</view>
					<view class="user_nick">
						<view class="nick_name">柏林</view>
						<view class="nick_tag">
						<!-- 	<text class="tag">举人</text>
							<text class="tag">品类3</text>
							<text class="tag">社群5</text> -->
						</view>
					</view>
					<view class="user_info">
						<text class="txt">个人主页</text>
						<image class="img" src="/static/person_info.png"></image>
					</view>
				</view>
				<view class="header_middle">
					<text class="middle_month">本月销量</text>
					<text class="middle_num">2315.00元</text>
				</view>
				<view class="header_bottom">
					<view class="bottom_item">
						<view class="item_top">
							<text class="top_num">0</text>元
						</view>
						<view class="item_bottom">
							<text class="bottom_balance">余额</text>
							<!-- <text class="bottom_money">提现</text> -->
						</view>
					</view>
					<view class="bottom_item">
						<view class="item_top">
							<text class="top_num">0</text>元
						</view>
						<view class="item_bottom">
							<text class="bottom_balance">未到账余额</text>
						</view>
					</view>
					<view class="bottom_item">
						<view class="item_top">
							<text class="top_num">0</text>元
						</view>
						<view class="item_bottom">
							<text class="bottom_balance">累计收入</text>
						</view>
					</view>
				</view>
				
			</view>
			<view class="orders">
				<navigator url="/pages/order/order"  hover-class="none">
					<view class="orders_top">
						<view class="top_left">我的订单</view>
						<view class="top_right">
							<text class="txt">全部订单</text>
							<image class="img" src="/static/order.png"></image>
						</view>
					</view>
				</navigator>
				<view class="orders_items">
					<navigator url="/pages/order/order"  hover-class="none">
						<view class="item">
							<image class="img" src="/static/order1.png"></image>
							<view class="txt">待付款</view>
						</view>
					</navigator>
					<navigator url="/pages/order/order"  hover-class="none">
						<view class="item">
							<image class="img" src="/static/order2.png"></image>
							<view class="txt">待发货</view>
						</view>
					</navigator>
					<navigator url="/pages/order/order"  hover-class="none">
						<view class="item">
							<image class="img" src="/static/order3.png"></image>
							<view class="txt">待收货</view>
						</view>
					</navigator>
					<navigator url="/pages/order/index"  hover-class="none">
						<view class="item">
							<image class="img" src="/static/order4.png"></image>
							<view class="txt">待评价</view>
						</view>
					</navigator>
					<navigator url="/pages/order/index"  hover-class="none">
						<view class="item">
							<image class="img" src="/static/order5.png"></image>
							<view class="txt">售后</view>
						</view>
					</navigator>
				</view>
			</view>
			<navigator url="/pages/person/person"  hover-class="none">
				<view class="info">
					<view class="info_left">
						<view class="left_top">完善个人资料</view>
						<view class="left_bottom">完善个人资料,可以获取更好的用户体验呦！</view>
					</view>
					<view class="info_right">完善</view>
				</view>
			</navigator>
		</view>
		<view class="lists">
			<navigator url="/pages/collect/collect"  hover-class="none">
				<view class="item">
					<image class="left_img" src="/static/collect.png"></image>
					<text class="left_txt">我的收藏</text>
					<image class="right_img" src="/static/my.png"></image>
				</view>     
			</navigator>
			<navigator url="/pages/discount/discount"  hover-class="none">
				<view class="item">
					<image class="left_img" src="/static/discount.png"></image>
					<text class="left_txt">优惠券</text>
					<image class="right_img" src="/static/my.png"></image>
				</view>    
			</navigator>
			<navigator url="/pages/mypush/mypush"  hover-class="none">
				<view class="item">
					<image class="left_img" src="/static/fabu.png"></image>
					<text class="left_txt">我的发布</text>
					<image class="right_img" src="/static/my.png"></image>
				</view>     
			</navigator>
			<navigator url="/pages/cart/cart"  hover-class="none">
				<view class="item">
					<image class="left_img" src="/static/carts.png"></image>
					<text class="left_txt">我的购物车</text>
					<image class="right_img" src="/static/my.png"></image>
				</view>     
			</navigator>
			<navigator url="/pages/mycard/mycard3"  hover-class="none">
				<view class="item">
					<image class="left_img" src="/static/card.png"></image>
					<text class="left_txt">银行卡</text>
					<image class="right_img" src="/static/my.png"></image>
				</view>     
			</navigator>
			
			<navigator url="/pages/address/address"  hover-class="none">
				<view class="item">
					<image class="left_img" src="/static/address.png"></image>
					<text class="left_txt">收货地址</text>
					<image class="right_img" src="/static/my.png"></image>
				</view>   
			</navigator>
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

	
.header{
    width:750upx;
    height: 354upx;
    background:rgb(255, 217, 68);
	.header_top{
		overflow: hidden;
		.user_img{
		    float: left;
		    width: 102upx;
		    height: 102upx;
		    margin: 14upx 27upx 0 33upx;
			background: #999;
			border-radius: 10upx;
		}
		.user_nick{
		    float: left;
		    margin-top:46upx;
			.nick_name{
				font-size: 40upx;
				line-height: 40upx;
				color: rgb(40, 40, 40);
			}
			.nick_tag{
				margin-top:8upx;
				height: 24upx;
				line-height: 24upx;
				.tag{
					display: inline-block;
					padding:3upx 12upx;
					font-size: 18upx;
					line-height: 18upx;
					background: #fff;
					border-radius: 30upx;
					margin-right:10upx;
				}
			}
		   
		}
		.user_info{
		    float: right;
		    margin:64upx 36upx 0 0;
		    width: 166upx;
		    height: 50upx;
		    border-radius: 20upx;
		    background:#FFFFFF; 
		    .txt{
		        font-size: 26upx;
		        color: rgb(40, 40, 40);
		        margin:0 18upx 0 18upx;
		    }
		    .img{
		        width: 12upx;
		        height: 20upx;
		    }
		}
	}
	.header_middle{
		margin-top:78upx;
		line-height:30upx;
		.middle_month{
			font-size: 24upx;
			color: rgb(40, 40, 40);
			margin-left: 40upx;
		}
		.middle_num{
			font-size: 30upx;
			color: rgb(40, 40, 40);
			margin-left: 35upx;
		}
	}
	.header_bottom{
		margin-top:30upx;
		width: 750upx;
		height: 96upx;
		background: #fff;
		border-top-left-radius:200upx;
		border-top-right-radius:200upx;
		.bottom_item{
			float: left;
			width: 250upx;
			height: 96upx;
			text-align: center;
			.item_top{
				font-size: 12upx;
				line-height: 30upx;
				margin-top:30upx;
				color: rgb(40, 40, 40);
				.top_num{
					font-size: 30upx;
					margin-right: 6upx;
				}
			}
			.item_bottom{
				line-height: 24upx;
				margin-top:12upx;
				.bottom_balance{
					font-size: 24upx;
				
					color: rgb(40, 40, 40);
				}
				.bottom_money{
					display: inline-block;
					font-size: 18upx;
					padding:0upx 12upx;
					border-radius: 20upx;
					color:#fff;
					background: #FF9265;
					margin-left: 14upx;
				}
				
			}
		}
	}
	
}
.orders{
    background:#fff;
    padding-top:51upx;
    .orders_top{
        overflow: hidden;
        .top_left{
            float: left;
            font-size: 30upx;
            line-height: 30upx;
            color: rgb(51, 51, 51);
            margin:0 0 0 32upx;
        }
        .top_right{
            float:right;
            line-height: 26upx;
            .txt{
                font-size: 26upx;
                color: rgb(152, 152, 152);
            }
            .img{
                width: 12upx;
                height: 20upx; 
                margin:0 36upx 0 9upx; 
            }
        
        }
    }
    .orders_items{
        overflow: hidden;
        padding-top:64upx;
        padding-bottom:36upx;
        .item{
            float: left;
            width: 150upx;
            text-align: center;
            .img{
                margin-bottom: 30upx;
                width:58upx;
                height: 62upx;
                margin: 0 auto;
            }
            .txt{
                font-size: 24upx;
                line-height: 24upx;
                color: rgb(40, 40, 40);
            }
        }
    }
}
.info{
    padding:26upx 54upx 34upx 58upx;
    margin-top:16upx;
    overflow: hidden;
    background: #FFFFFF;
    .info_left{
        float: left;
        .left_top{
            
            font-size: 30upx;
            line-height: 30upx;
            font-weight: bold;
            color: rgb(40,40, 40);  
        }
        .left_bottom{
            margin-top:20upx;
            font-size: 24upx;
            line-height: 24upx;
            font-weight: bold;
            color: rgb(102,102, 102);  
        }
    }
    .info_right{
        float: right;
        margin-top:16upx;
        width: 152upx;
        height: 52upx;
        background: #FFD944;
        font-size: 24upx;
        color:rgb(40, 40, 40);
        line-height: 52upx;
        text-align: center;
        border-radius: 10upx;
    }
}
.lists{
    margin-top:16upx;
	margin-bottom: 100upx;
    .item{
        padding:32upx 35upx;
        background: #fff;
        overflow: hidden;
        .left_img{
            float: left;
            width:36upx;
            height: 36upx;
            vertical-align:bottom;  
        }
        .left_txt{
            float: left;
            margin-top:4upx;
            font-size: 32upx;
            line-height: 32upx;
            color: rgb(51,51,51);
            margin-left: 23upx;
        }
        .right_img{
            float: right;
            margin-top: 5upx;
            width:16upx;
            height: 27upx;
            vertical-align:bottom;
        }
    }
}
</style>
