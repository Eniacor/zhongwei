<template>
	<view>
		<view class="birthday">
			<view class="birday_time" bindtap="onPopupOpen">
				<view class="time_left">年龄</view>
				<view class="time_right">23岁</view>
			</view>
			<view class="birday_star" bindtap="onPopupOpen1">
				<view class="time_left">星座</view>
				<view class="time_right">金牛座</view>
			</view>
			<view class="btn" >保存</view>
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
.birthday{
    .birday_time{
        overflow: hidden;
        padding:36rpx 32rpx;
        border-bottom: 1rpx solid #f2f2f2;
        background: #fff;
        .time_left{
            float: left;
            font-size: 30rpx;
            line-height: 30rpx;
            color: rgb(51, 51, 51); 
        }
        .time_right{
            float: left;
            font-size: 30rpx;
            line-height: 30rpx;
            color: rgb(51, 51, 51); 
            margin-left: 58rpx;
        }
    }
    .birday_star{
        overflow: hidden;
        padding:36rpx 32rpx;
        background: #fff;
        .time_left{
            float: left;
            font-size: 30rpx;
            line-height: 30rpx;
            color: rgb(51, 51, 51); 
        }
        .time_right{
            float: left;
            font-size: 30rpx;
            line-height: 30rpx;
            color: rgb(51, 51, 51); 
            margin-left: 58rpx;
        }
    }
    .btn{
		margin-left:33rpx;
		margin-top:148rpx;
		text-align: center;
		width:684rpx;
		height:82rpx;
		line-height: 86rpx;
		background:#FFD944;
		color:rgb(51, 51, 51);
		border-radius: 16rpx;
		outline: none;
    }
}
</style>
