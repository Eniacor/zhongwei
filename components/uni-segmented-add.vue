<template>
	<view class="segmented-add" :class="styleType" :style="wrapStyle">
		<view v-for="(item, index) in values" class="segmented-add-item" :class="styleType" :key="index" :style="index === currentIndex ? activeStyle : itemStyle" @click="onClick(index)">
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
				default: '#000'
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
	.segmented-add {
		display: flex;
		justify-content:space-around;
		align-items: center;
		width:100%;
		height:82upx;
		background: rgb(255, 217, 68);
	}

	.segmented-add.text {
		border: 0;
		border-radius: 0upx;
	}


	.segmented-add-item {
		display: inline;
		padding-top:28upx;
		padding-bottom:14upx;
		padding-left: 0!important;
		padding-right: 0!important;
		font-size: 30upx;
		line-height: 30upx;
	}

	.segmented-add-item.button {
		border-left: 1upx solid;
	}

	.segmented-add-item.text {
		border-left: 0;
		font-size:30upx;
		color:#666666;
	}

	.segmented-add-item:first-child {
		border-left-width: 0;
	}
</style>
