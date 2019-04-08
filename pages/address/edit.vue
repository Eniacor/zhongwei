<template>
	<view>
		<view class="lists">
			<view class="item">
				<input class="left_txt" placeholder="收货人" />
				<image class="right_img" src="/static/my.png"></image>
			</view>
			<view class="item">
				<input class="left_txt" placeholder="手机号码" />
			</view>
			<view class="item">
				<input class="left_txt" placeholder="配送地址" />
			</view>
			<view class="item">
				<textarea class="left_textarea" placeholder="详细地址: 如宿舍楼栋号、单元室等"/>
			</view>
		</view>
		<view class="bottom">
			<label class="txt">
				<radio value="r1" checked="true" color="red"/>设置为默认地址
			</label>
		</view>
		<view class="delete">
			删除收获地址
		</view>
		<view class="btn">添加地址</view>
	</view>
	
</template>
<script>
	export default {
		data() {
			return {
		
			}
		},
		methods: {
		
		}
	}
</script>

<style lang="scss">
	page {
		height: auto;
		min-height: 100%;
	}
	.lists{
	    .item{
	        padding:36upx 0upx;
			padding-left:32upx;
			padding-right: 32upx;
	        background: #fff;
	        overflow: hidden;
			border-bottom: 1upx solid #f2f2f2;
	        .left_txt{
	            float: left;
	            font-size: 32upx;
	            line-height: 32upx;
	            color: rgb(51,51,51);
				width: 660upx;
	        }
			.left_textarea{
				float: left;
				height: 90upx;
				font-size: 32upx;
				line-height: 32upx;
				color: rgb(51,51,51);
				width: 660upx;
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
	.bottom{
		margin-top:42upx;
		padding:36upx 0upx;
		padding-left:32upx;
		padding-right: 32upx;
		background: #fff;
		overflow: hidden;
		border-bottom: 1upx solid #f2f2f2;
		.txt{
			font-size: 32upx;
			color: #999!important;
		}
	}
	.delete{
		height: 100upx;
		font-size: 32upx;
		line-height: 100upx;
		color: red;
		background: #fff;
		padding-left:30upx;
	}
	.btn{
		margin-left:33rpx;
		margin-top:352rpx;
		width:684rpx;
		height:82rpx;
		line-height: 86rpx;
		background:#FFD944;
		color:rgb(51, 51, 51);
		border-radius: 16rpx;
		outline: none;
		text-align: center;
    }
</style>
