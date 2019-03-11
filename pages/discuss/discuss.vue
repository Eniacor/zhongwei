<template>
	<view>
		<view class="discuss">
			<view class="top">
				<image class="top_img"></image>
				<view class="top_txt">BEELY彼丽四味组汤 足浴包 脚药包 一盒10袋 共40袋...</view>
			</view>
			<view class="content">
				<view class="content_txt">
					<textarea placeholder="分享购买心得给想买的他们吧～" class="custom_textarea" />
					</view>
        <view class="content_img">
            <view class="img_item">
                <image class="item_circle" src="/static/discuss2.png"></image>
                <view class="item_txt">添加照片</view>
            </view>
            <view class="video_item">
                <image class="item_circle" src="/static/discuss1.png"></image>
                <view class="item_txt">添加视屏</view>
            </view>
        </view>
    </view>
    <view class="btn" sizetype="default"  bind:click="handleData">发表</view>
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
.discuss{
    .top{
        overflow: hidden;
        padding:5rpx 32rpx 18rpx 32rpx;
        .top_img{
            float: left;
            width: 66rpx;
            height: 66rpx;
            background:#A6A6A6; 
        } 
        .top_txt{
            float: left;
            margin-left:22rpx;
            margin-top:20rpx;
            font-size: 24rpx;
            line-height: 24rpx;
            color:rgb(51, 51, 51);
        }
    }
    .content{
        padding:54rpx 32rpx 54rpx;
        background: #fff;
        .content_txt{
            .custom_textarea{
                width: 686rpx!important;
                height: 150rpx!important;
                font-size: 30rpx;
                line-height: 30rpx;
                color:#707070;
            }
        }
        .content_img{
            overflow: hidden;
            .img_item{
                float: left;
                width: 150rpx;
                height: 150rpx;
                border:4rpx dotted #8E8E93; 
                margin-right: 21rpx;
                .item_circle{
					display: block;
                    width: 48rpx;
                    height: 48rpx;
                    margin:0 auto;
                    margin-top:36rpx;
                }
                .item_txt{
                    font-size:24rpx;
                    line-height:24rpx;
                    color:#8E8E93;
                    text-align: center;
                    margin-top:24rpx;
                }
            }
            .video_item{
                float: left;
                width: 150rpx;
                height: 150rpx;
                border:4rpx dotted #8E8E93; 
                .item_circle{
					display: block;
                    width: 48rpx;
                    height: 48rpx;
                    margin:0 auto;
                    margin-top:36rpx;
                }
                .item_txt{
                    font-size:24rpx;
                    line-height:24rpx;
                    color:#8E8E93;
                    text-align: center;
                    margin-top:24rpx;
                }
            }
        }
    }
    .btn{
      
		margin-left:33rpx;
		margin-top:350rpx;
		width:684rpx;
		height:82rpx;
		line-height: 86rpx;
		background:#FFD944;
		color:rgb(51, 51, 51);
		border-radius: 16rpx;
		outline: none;
		text-align: center;
    }
}
</style>
