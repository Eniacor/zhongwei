<template>
	<view class="segmented-control" :class="styleType" :style="wrapStyle">
		<view v-for="(item, index) in values" class="segmented-control-item" :class="styleType" :key="index" :style="index === currentIndex ? activeStyle : itemStyle" @click="onClick(index)">
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
						styleString = `color:#666;border-left:0;`;
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
						styleString = `color:#000;border-color:${this.activeColor};border-left:0;border-bottom-style:solid;`;
						break;
					default:
						styleString = `color:#fff;border-color:${this.activeColor};background-color:${this.activeColor}`;
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
	.segmented-control {
		display: flex;
		justify-content:space-around;
		align-items: center;
		width:100%;
		height:82upx;
		background: rgb(255, 217, 68);
	}

	.segmented-control.text {
		border: 0;
		border-radius: 0upx;
	}


	.segmented-control-item {
		display: inline;
		padding-top:42upx;
		padding-bottom:18upx;
		padding-left: 0!important;
		padding-right: 0!important;
		font-size: 30upx;
		line-height: 30upx;
	}

	.segmented-control-item.button {
		border-left: 1upx solid;
	}

	.segmented-control-item.text {
		border-left: 0;
		font-size:30upx;
		color:#666666;
	}

	.segmented-control-item:first-child {
		border-left-width: 0;
	}
</style>
