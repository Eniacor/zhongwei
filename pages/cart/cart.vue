<template>
	<view>
		<view class='container' v-if="iscart">
			<view class='section section-good'>
				<view class='section-bottom'>
					<checkbox-group @change="selectalltap">
						<label class='checkbox-allcheck'>
							<checkbox value="!checkAll" :checked="checkAll" hidden='hidden' />
							<!-- <icon type="circle" size="22" v-if="!checkAll"></icon>
							<icon type="success" color="#D41C1C" size="22" v-if="checkAll"></icon> -->
							<text class='check-all-text'>中微直供</text>
						</label>
					</checkbox-group>
				</view>
				<checkbox-group @click="checkboxChange">
					<view class='good' v-for='(good,index) in goodList'>
						<view class='good_content'>
							<view class='good_checkbox'>
								<label class="checkbox">
									<checkbox :value="good.isbn" :checked="good.checked" hidden='hidden' />
									<!-- <icon type="circle" size="22" v-if="!good.checked"></icon>
									<icon type="success" color="#D41C1C" size="22" v-if="good.checked"></icon> -->
								</label>
							</view>
							<image class='good_img'></image>
							<view class='right'>
								<view class='right_title'>小米 红色6 Pro 全网通手机 双卡双...</view>
								<view class='right_des'>规格4+32 颜色：巴黎蓝</view>
								<view class='right_account'>库存紧张</view>
								<view class='right_price'>￥118</view>
								<view class='stepper'>
									<view class='subtract' @click='subtracttap(index)'>-</view>
									<input class='count' type='number' :value="good.count"></input>
									<view class='add' @click="addtap(index)">+</view>
								</view> 
								<image  class="delete" src='/static/delete.png' @click="deleteList"></image>
							</view>
						</view>
					</view>
				</checkbox-group>
			</view>
		</view>
		<view class='bottom'>
			<view class='total'>总计：
				<text>¥{{totalPrice}}</text>
			</view>
			<navigator  url=''>
				<view class='go'>继续选购</view>
			</navigator>
			<navigator url=''>
				<view class='btn' :class="[totalCount > 0 ? 'btn-primary' : 'btn-default']">去结算({{totalCount}})</view>
			</navigator>
		</view> 
		<!--如果购物车内没有数据，就显示没有数据-->  
		<view class="cartList" v-if="!iscart">  
			<image src="/assets/images/iconfont-cart-empty.png"/>  
			<view>购物车什么都没有，赶快去购物吧</view>  
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				iscart: true, //控制购物车有没有数据
				goodList: [
				  {
					'cover': '/assets/images/img/132-12.jpg',
					'isbn': '9787535482051',
					'desc': '【光山馆】2斤大连烟台樱桃新鲜水果现摘现发产地直供孕妇水果儿童水果当季水果早大果红灯美早车厘子大樱桃 2斤 AAA级 果径28mm以上',
					'price': 25.9,
					'count': 1,
					'checked': false
				  },
				  {
					'cover': '/assets/images/img/0112-154.jpg',
					'isbn': '9787540455958',
					'desc': '【第二件立减20元】新鲜采摘 国产 美早 车厘子 大樱桃新鲜水果1kg 单果26-28mm',
					'price': 20.5,
					'count': 1,
					'checked': false
				  },
				],
				checkAll: false,
				totalCount: 0,
				totalPrice: 0,
			};
		},
		components: {
		},
		methods:{
			/**
			  * 删除购物车当前商品
			  */
			deleteList(e) {
				let index = e;
				let goodList = this.goodList;
				goodList.splice(index, 1);
				this.goodList=goodList;
				if (!goodList.length) {
					this.iscart=true;
				} else {
					this.calculateTotal();
				}
			},
			/**
			  * 计算商品总数
			  */
			calculateTotal: function () {
				let goodList = this.goodList;
				let totalCount = 0;
				let totalPrice = 0;
				for (let i = 0; i < goodList.length; i++) {
					let good = goodList[i];
					if (good.checked) {
						totalCount += good.count;
						totalPrice += good.count * good.price;
					}
				}
				totalPrice = totalPrice.toFixed(2);
				this.totalCount= totalCount;
				this.totalPrice=totalPrice;
			},
			/**
			  * 用户点击商品减1
			  */
			subtracttap: function (e) {
				let index = e;
				let goodList = this.goodList;
				let count = goodList[index].count;
				if (count <= 1) {
					return;
				} else {
					goodList[index].count--;
					this.goodList=goodList;
					this.calculateTotal();
				}
			},
			/**
			  * 用户点击商品加1
			  */
			addtap: function (e) {
				let index = e;
				let goodList = this.goodList;
				var count = goodList[index].count;
				goodList[index].count++;
				this.goodList=goodList;
				this.calculateTotal();
			},
			/**
			  * 用户选择购物车商品
			  */
			checkboxChange: function (e) {
				let checkboxItems = this.goodList;
				let values = e;
				for (let i = 0; i < checkboxItems.length; ++i) {
					checkboxItems[i].checked = false;
					for (let j = 0; j < values.length; ++j) {
						if (checkboxItems[i].isbn == values[j]) {
							checkboxItems[i].checked = true;
							break;
						}
					}
				}
				let checkAll = false;
				if (checkboxItems.length == values.length) {
					checkAll = true;
				}
				this.goodList=checkboxItems;
				this.checkAll=checkAll;
				this.calculateTotal();
			},
			/**
			   * 用户点击全选
			   */
			selectalltap: function (e) {
				var value = e.detail.value;
				var checkAll = false;
				if (value && value[0]) {
					checkAll = true;
				}
				var goodList = this.goodList;
				
				for (var i = 0; i < goodList.length; i++) {
				  var good = goodList[i];
				  good['checked'] = checkAll;
				}
				this.checkAll=checkAll;
				this.goodList=goodList;
				this.calculateTotal();
			}
		}
		
	}
</script>

<style lang="scss">
	.container {
		width: 100%;
		min-height: 100%;
		display: flex;
		flex-direction: column;
		box-sizing: border-box;
	}
	.good {
		border-top: 1px solid #f2f2f2;
		border-bottom: 1px solid #f2f2f2;
		background-color: #fff;
		.good_content {
			z-index:1; 
			width:100%;
			height:257upx;
			background-color:#fff;
			.checkbox {
				float: left;
				width: 38upx;
				height: 38upx;
				margin-left:30upx;
				margin-right: 14upx;
				margin-top:110upx;
			}
			.good_img {
				float:left;
				margin-top:39upx;
				width: 179upx;
				height:179upx;
				background: #8E8E93;
			}
			.right{
				position: relative;
				float: left;
				margin-left:12upx;
				.right_title{
					width: 426upx;
					margin-top:26upx;
					font-size: 26upx;
					line-height: 26upx;
					color:#333;
				}
				.right_des{
					width: 426upx;
					margin-top:25upx;
					font-size: 24upx;
					line-height: 24upx;
					color:#A7A7A7;
				}
				.right_account{
					width: 426upx;
					margin-top:36upx;
					font-size: 26upx;
					line-height: 26upx;
					color:#FF000D;
				}
				.right_price{
					width: 426upx;
					margin-top:26upx;
					font-size: 26upx;
					line-height: 26upx;
					color:#FF000D;
				}
				.stepper {
					position: absolute;
					top:144upx;
					right:32upx;
					overflow: hidden;
					margin-top: 10upx;
					width: 50%;
					margin-left: 70upx;
					.add,.subtract{
						float: left;
						width: 64upx;
						height:64upx;
						line-height:64upx;
						text-align: center;
						font-size: 30upx;
						border: 1px solid #ccc;
						box-sizing: border-box;
						color:#333;
					}
					.count {
						float: left;
						width: 64upx;
						height:64upx;
						line-height:64upx;
						border-top: 1px solid #ccc;
						border-bottom: 1px solid #ccc;
						text-align: center;
						box-sizing: border-box;
						min-height: 1rem;
						font-size: 28upx;
					}
					.disabled {
						float: left;
						color: #eee;
					}
				} 
				.delete{
					position: absolute;
					top:168upx;
					right:-11upx;        
					width: 34upx;
					height: 34upx;
				}
			}
		}
	}
	.section-bottom {
		display: flex;
		flex-direction: row;
		align-items: center;
		width: 100%;
		height: 100upx;
		margin-bottom: 0;
		background-color: #fff;
		box-sizing: border-box;
		z-index: 99;
	}
  
  .section-bottom .btn {
		width: 160upx;
		height: 100upx;
		line-height: 100upx;
		text-align: center;
		color: #fdfffd;
		background-color: #fbb304;
  }
  
  .section-bottom .btn-default {
    color: #363636;
    background-color: #eee;
  }
  
  .section-bottom .btn-primary {
    color: #fdfffd;
    background-color: #e83632;
  }
  
  .section-bottom .checkbox-allcheck {
    display: inline-block;
    margin-left: 30upx;
    vertical-align: top;
    font-size: 0px;
  }
  
  .section-bottom .check-all-text {
    display: inline-block;
    vertical-align: top;
    margin-left: 10upx;
    height: 23px;
    line-height: 23px;
    font-size: 28upx;
  }
  
  .section-bottom .total {
    flex: 1;
    text-align: center;
    font-size: 26upx;
  }
  
  .total .totalCount {
    font-size: 26upx;
    display: inline-block;
    vertical-align: middle;
  }
  
  .total .totalPrice {
    display: inline-block;
    font-size: 26upx;
    margin-left: 20upx;
    vertical-align: middle;
  }
  
  .total .totalCount text {
    color: #e4452a;
    vertical-align: middle;
  }
  
  .total .totalPrice text {
    color: #e4452a;
    font-size: 36upx;
    vertical-align: middle;
  }
  
  
  /*   空购物车  */
  .cartList {  
    padding: 100px 0 0 0;  
    display: flex;  
    justify-content: center;  
    flex-direction: column;  
    align-items: center;  
    color: #999;  
  }  
    
  .cartList image {  
    width: 66px;  
    height: 66px;  
    margin-bottom: 20px;  
  }  

.bottom{
  position: fixed;
  bottom: 0;
  width: 750upx;
  line-height:100upx;
  background: #fff;
  border-top:1upx solid #f2f2f2;
  font-size: 30upx;
  color: #333;
  z-index:100; 
  .total{
    float: left;
    text-align:center;
    width: 249upx;
    height: 100upx;
	line-height: 100upx;
    border-right: 1upx solid #f2f2f2;
  }
  .go{
    float: left;
    text-align:center;
	line-height: 100upx;
    width: 249upx;
    height: 100upx;
    border-right: 1upx solid #f2f2f2;
  }
  .btn{
    float: left;
    text-align:center;
    width: 250upx;
    height: 100upx;
	line-height: 100upx;
    background: #FF000D;
    color:#fff;
  }
}
</style>
