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
				<view class="avatar_title">基本信息</view>
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
					<view class="right_txt">柏林</view>
					<image class="right_img" src="/static/my.png"></image>
				</view>
			</navigator>
			<navigator url="/pages/sex/sex" hover-class="none">
				<view class="item">
					<text class="left_txt">性别</text>
					<view class="right_txt">男</view>
					<image class="right_img" src="/static/my.png"></image>
				</view>
			</navigator>
			<navigator url="/pages/birthday/birthday" hover-class="none">
				<view class="item">
					<text class="left_txt">生日</text>
					<view class="right_txt">1994-04-18</view>
					<image class="right_img" src="/static/my.png"></image>
				</view>
			</navigator>
			<navigator url="/pages/profession/profession" hover-class="none">
				<view class="item">
					<text class="left_txt">专业</text>
					<view class="right_txt">UI设计</view>
					<image class="right_img" src="/static/my.png"></image>
				</view>
			</navigator>
			<navigator url="/pages/school/index" hover-class="none">
				<view class="item">
					<text class="left_txt">院校名称</text>
					<view class="right_txt">盐城学院</view>
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
    width: 750upx;
    height: 60upx;
    background: #fff;
    padding-top:28upx;
    .progress{
        width: 511upx;
        height: 32upx;
        margin: 0 auto;
        position: relative;
        .progress_back{
            position: absolute;
            width: 511upx;
            height: 32upx;
            background:#EDEAF1; 
            z-index: 0;
            border-radius:20upx; 
        }
        .progress_color{
            position: absolute;
            width: 15%;
            height: 32upx;
            background:#FFD944;
            z-index: 0; 
            border-radius:20upx; 
        }
        .progress_txt{
            position: absolute;
            top:9upx;
            left:42%;
            font-size: 16upx;
            line-height: 16upx;
            color:#333;
        }
    }
}
.avatar{
	.avatar_title{
		margin-top:56upx;
		margin-bottom: 12upx;
		font-size: 24upx;
		margin-left: 35upx;
	}
  
    .item{
		position: relative;
        height: 136upx;
        background: #fff;
        .left_txt{
			position: absolute;
			top:53upx;
			left:35upx;
            font-size: 32upx;
            line-height: 32upx;
            color: rgb(51,51,51);
        }
        .right_img1{
			position: absolute;
			top:21upx;
			right:90upx;
            width:94upx;
            height: 94upx;
            border-radius: 10upx;
            background: #EDEAF1;
        }
        .right_img{
			position: absolute;
			top:55upx;
			right:35upx;
            width:16upx;
            height: 27upx;
        }
    }
}
.lists{
    margin-top:16upx;
    .item{
		height:32upx;
        padding:32upx 35upx;
        background: #fff;
        position: relative;
        .left_txt{
			position: absolute;
			top:32upx;
			left:35upx;
            font-size: 32upx;
            line-height: 32upx;
            color: rgb(51,51,51);
        }
        .right_img{
			position: absolute;
			top:35upx;
			right:35upx;
            width:16upx;
            height: 27upx;
        }
		.right_txt{
			position: absolute;
			top:32upx;
			right:70upx;
			font-size: 32upx;
			line-height: 32upx;
			color: #999;
		}
    }
}
</style>
