<template>
	<view>
		<view class="top">
			<view class="progress">
				<view class="progress_back"></view>
				<view class="progress_color"></view>
				<view class="progress_txt">完整度15%</view>
			</view>
		</view>

		<navigator url="" hover-class="none">
			<view class="avatar">
				<view class="avatar_title"></view>
				<view class="item">
					<text class="left_txt">头像</text>
					<image class="right_img" src="/static/my.png"></image>
					<view class="right_img1"></view>
				</view>
			</view>
		</navigator>

		<view class="lists">
			<navigator url="/pages/nickname/nickname" hover-class="none">
				<view class="item">
					<text class="left_txt">昵称</text>
					<image class="right_img" src="/static/my.png"></image>
				</view>
			</navigator>
			<navigator url="/pages/sex/sex" hover-class="none">
				<view class="item">
					<text class="left_txt">性别</text>
					<image class="right_img" src="/static/my.png"></image>
				</view>
			</navigator>
			<navigator url="/pages/birthday/birthday" hover-class="none">
				<view class="item">
					<text class="left_txt">生日</text>
					<image class="right_img" src="/static/my.png"></image>
				</view>
			</navigator>
			<navigator url="/pages/profession/profession" hover-class="none">
				<view class="item">
					<text class="left_txt">专业</text>
					<image class="right_img" src="/static/my.png"></image>
				</view>
			</navigator>
			<navigator url="/pages/school/index" hover-class="none">
				<view class="item">
					<text class="left_txt">院校名称</text>
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
.top{
    width: 750rpx;
    height: 60rpx;
    background: #fff;
    padding-top:28rpx;
    .progress{
        width: 511rpx;
        height: 32rpx;
        margin: 0 auto;
        position: relative;
        .progress_back{
            position: absolute;
            width: 511rpx;
            height: 32rpx;
            background:#EDEAF1; 
            z-index: 0;
            border-radius:20rpx; 
        }
        .progress_color{
            position: absolute;
            width: 15%;
            height: 32rpx;
            background:#FFD944;
            z-index: 0; 
            border-radius:20rpx; 
        }
        .progress_txt{
            position: absolute;
            top:9rpx;
            left:42%;
            font-size: 16rpx;
            line-height: 16rpx;
            color:#333;
        }
    }
}
.avatar{
    margin-top:16rpx;
    .item{
        height: 136rpx;
        background: #fff;
        overflow: hidden;
        .left_txt{
            float: left;
            margin-top:53rpx;
            font-size: 32rpx;
            line-height: 32rpx;
            color: rgb(51,51,51);
            margin-left: 35rpx;
        }
        .right_img1{
            float: right;
            margin-top:21rpx;
            width:94rpx;
            height: 94rpx;
            border-radius: 10rpx;
            background: #EDEAF1;
        }
        .right_img{
            float: right;
            margin-top: 5rpx;
            width:16rpx;
            height: 27rpx;
            vertical-align:bottom;
            margin-left:42rpx;
            margin-right: 35rpx;
            margin-top:55rpx;

        }
    }
}
.lists{
    margin-top:16rpx;
    .item{
        padding:32rpx 35rpx;
        background: #fff;
        overflow: hidden;
        .left_img{
            float: left;
            width:36rpx;
            height: 36rpx;
            vertical-align:bottom;  
        }
        .left_txt{
            float: left;
            margin-top:4rpx;
            font-size: 32rpx;
            line-height: 32rpx;
            color: rgb(51,51,51);
        }
        .right_img{
            float: right;
            margin-top: 5rpx;
            width:16rpx;
            height: 27rpx;
            vertical-align:bottom;
        }
    }
}
</style>
