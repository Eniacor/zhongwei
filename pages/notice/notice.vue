<template>
	<view>
		<view style="background: #fff;">
			<uni-segmented-control :current="current" :values="items" v-on:clickItem="onClickItem">
			</uni-segmented-control>
		</view>
		<view class="content">
			<view v-show="current === 0">
				<view class="book">
					<view class="book_left">
						<view class="left_title">
							在校园如何潜移默化做推广销售
						</view>
						<view class="left_bottom">
							<text class="bottom_name">中微直供</text>
							<text class="bottom_date">2019-01-23</text>
						</view>
					</view>
					<view class="book_right">
						<image class="right_img" src=""></image>
					</view>
				</view>
			</view>
			<view v-show="current === 1">
				<view class="book">
					<view class="book_left">
						<view class="left_title">
							在校园如何潜移默化做推广销售
						</view>
						<view class="left_bottom">
							<text class="bottom_name">中微直供</text>
							<text class="bottom_date">2019-01-23</text>
						</view>
					</view>
					<view class="book_right">
						<image class="right_img" src=""></image>
					</view>
				</view>
			</view>
			<view v-show="current === 2">
				<view class="question">
					<textarea class="question_txt" value="" placeholder="请提出您的意见和建议,我们将会对您的问题作出反馈" />
				</view>
				<view class="btn">提交</view>
			</view>
		</view>
	</view>
</template>

<script>
	import uniSegmentedControl from '../../components/uni-segmented-control.vue';
	export default {
		data() {
			return {
				items: [
					'系统消息',
					'我的消息',
					'问题反馈',
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

	.book {
		overflow: hidden;
		background: #fff;
		height: 258upx;
		border: 1upx solid transparent;
		border-top-color: #f2f2f2;

		.book_left {
			float: left;
			margin-top: 55upx;
			margin-left: 45upx;

			.left_title {
				width: 384upx;
				height: 88upx;
				font-size: 32upx;
				line-height: 46upx;
				color: rgb(0, 0, 0);
			}

			.left_bottom {
				width: 388upx;
				line-height: 22upx;
				margin-top: 25upx;

				.bottom_name {
					font-size: 22upx;
					line-height: 22upx;
					color: #666;
					margin-right: 12upx;
					vertical-align: middle;
				}

				.bottom_date {
					font-size: 22upx;
					line-height: 22upx;
					color: #666;
					vertical-align: middle;
				}
			}
		}

		.book_right {
			float: right;
			margin-top: 36upx;
			margin-right: 30upx;
			width: 226upx !important;
			height: 154upx !important;
			background: #666;
			border-radius: 10upx;
		}
	}
	.question{
		width: 630upx;
		height: 284upx;
		border-radius: 10upx;
		background: #fff;
		padding:30upx 42upx;
		margin: 0 auto;
		margin-top:35upx;
		.question_txt{
			width: 630upx;
			height: 200upx;
			font-size: 30upx;
		}
	}
	.btn{
		width: 690upx;
		height:92upx;
		background: rgb(255,217,68);
		line-height: 92upx;
		border-radius: 10upx;
		text-align: center;
		margin:0 auto;
		margin-top:654upx;
	}
</style>
