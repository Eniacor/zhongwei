<template>
	<view class="button-control" :class="styleType" :style="wrapStyle">
		<view v-for="(item, index) in values" class="button-control-item" :class="styleType" :key="index" :style="index === currentIndex ? activeStyle : itemStyle" @click="onClick(index)">
			{{item}}
		</view>
	</view>
</template>

<script>
	export default {
		name: 'segmented-control',
		props: {
			current: {
				type: Number,
				default: 0
			},
			values: {
				type: Array,
				default () {
					return [];
				}
			},
			activeColor: {
				type: String,
				default: '#FFD944'
			},
			styleType: {
				type: String,
				default: 'text'
			}
		},
		data() {
			return {
				currentIndex: this.current
			}
		},
		watch: {
			current(val) {
				if (val !== this.currentIndex) {
					this.currentIndex = val;
				}
			}
		},
		computed: {
			wrapStyle() {
				let styleString = '';
				switch (this.styleType) {
					case 'text':
						styleString = `border:0;`;
						break;
					default:
						styleString = `border-color: ${this.activeColor}`;
						break;
				}
				return styleString;
			},
			itemStyle() {
				let styleString = '';
				switch (this.styleType) {
					case 'text':
						styleString = `color:#000;border-left:0;`;
						break;
					default:
						styleString = `color:${this.activeColor};border-color:${this.activeColor};`;
						break;
				}
				return styleString;
			},
			activeStyle() {
				let styleString = '';
				switch (this.styleType) {
					case 'text':
						styleString = `color:#fff;background:#CE4031;`;
						break;
					default:
						styleString = `color:#fff;border-color:#CE4031;background:#CE4031;`;
						break;
				}
				return styleString;
			}
		},
		methods: {
			onClick(index) {
				if (this.currentIndex !== index) {
					this.currentIndex = index;
					this.$emit('clickItem', index);
				}
			}
		},
	}
</script>

<style>
	.button-control {
		display: flex;
		justify-content:space-around;
		align-items: center;     /* 垂直居中 */
		width:100%;
		height:82upx;
		border: 1px solid red;
	}
	.button-control-item {
		display: inline;
		padding:26upx 0;
		border-bottom: 1upx solid #007AFF;
		background-color: red;
		font-size: 30upx;
		line-height: 30upx;
	}
	/* .segmented-control {
		display:flex;
		padding-top:24rpx;
        padding-left:29rpx;
		flex-direction: row;
		flex-wrap:wrap;
		font-size:30upx;
		box-sizing: border-box;
	}
	.segmented-control-item {
		margin-right:24upx;
        margin-bottom:21upx;
		padding: 20upx;
		font-size: 26upx;
		line-height: 26upx;
		box-sizing: border-box;
		background: #FBF0EF;
		border-radius: 8rpx;
	} */
</style>
