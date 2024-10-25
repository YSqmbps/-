	<template>
		<view class="">

			<!--  公告部分 -->
			<view
				style="padding: 5px 0px;  background-color: #04DE46; display: flex; align-items: center; overflow: hidden; white-space: nowrap;">
				<view style="z-index: 100;background-color: #04DE46;padding-left: 10px;"><uni-icons type="sound" size="20"></uni-icons></view>
				<view style="z-index: 1;" class="scroll-text" v-bind:style="scrollStyle">{{ scrollContent }}</view>
			</view>



			<!-- 4个功能 -->
			<view class="nsetFunctions">
				<view class="func" style="left: -5px; top:-3px">
					<view class="text">扫码绑定</view>
					<view class="icon iconfont icon-saoyisaosaoma"></view>
				</view>
				<view class="func" style="left: 175px; top:-77px">
					<view class="text">添加鸟巢</view>
					<view class="icon iconfont icon-a-ziyuan18"></view>
				</view>
				<view class="func" style="left: -5px; top:-84px">
					<view class="text">鸟巢详情</view>
					<view class="icon iconfont icon-16"></view>
				</view>
				<view class="func" style="left: 175px; top:-158px">
					<view class="text">养鸟日志</view>
					<view class="icon iconfont icon-rizhi1"></view>
				</view>
			</view>


			<!-- 鸟巢情况 -->
			<view class="nestSituation">
				<view class="nestSituation-container">
					<view class="currentNest">
						<view class="icon iconfont icon-niaochao" style="position: relative; left: 5rpx; width: 65rpx;"></view>
						<view class="currentNest-text">
							<text>当前鸟巢</text>
						</view>
					</view>

					<!-- 3个功能 -->
					<view class="views">
						<view class="views-container">
							<view class="views-func">地图</view>
							<view class="views-func-detail">查看我的鸟巢</view>
							<view class="icon iconfont icon-ditu" style="position: relative; left: 137rpx; top: -47rpx;">
							</view>
						</view>

						<view class="views-container">
							<view class="views-func">警告</view>
							<view class="views-func-detail">查看鸟巢预警</view>
							<view class="icon iconfont icon-jinggao" style="position: relative; left: 137rpx; top: -47rpx;"></view>
						</view>

						<view class="views-container">
							<view class="views-func">知识</view>
							<view class="views-func-detail">查看育鸟心得</view>
							<view class="icon iconfont icon-zhishi" style="position: relative; left: 137rpx; top: -47rpx;">
							</view>
						</view>
					</view>
				</view>
			</view>

			<!-- 图片 -->
			<image src="@/static/pexels-juan-felipe-ramirez-312591454-28116664.jpg" mode="" class="bird-image"></image>
		</view>
	</template>
	</template>


	<script>
		export default {
			data() {
				return {
					scrollContent: '江西农业大学是一所以农业为优势、以生物技术为特色、多学科协调发展的农业大学。该校位于江西省南昌市，具有博士学位授予权，是我国首批具有学士学位、硕士学位授予权单位之一，也是江西省最早开展研究生教育的单位。'
				};
			},
			computed: {
				// 计算属性，可以动态修改文本效果  
				scrollStyle() {
					return {
						width: `${this.scrollContent.length}em`,
					};
				}
			}
		}
	</script>

	<style>
		.scroll-text {
			font-size: 12px;
			display: inline-block;
			animation: scroll 18s linear infinite;
			/* 动画持续时间和速度可以调整 */
		}

		@keyframes scroll {
			0% {
				transform: translateX(100%);
				/* 初始位置在视口外 */
			}

			100% {
				transform: translateX(-100%);
				/* 到达视口外 */
			}
		}

		.nsetFunctions {
			display: flex;
			flex-wrap: wrap;
			justify-content: space-between;
			margin-top: 10px;
			margin-left: 25rpx;
			width: 700rpx;
			height: 266rpx;
			position: relative;
			top: -10rpx;
			box-sizing: border-box;
			/* background-color: antiquewhite; */
		}

		.func {
			display: flex;
			align-items: center;
			justify-content: center;
			position: relative;
			margin: 15rpx 25rpx;
			width: 310rpx;
			height: 60px;
			background-color: #34D762;
			/* border: 1px solid; */
			border-radius: 5%;
			box-sizing: border-box;
			position: relative;
		}


		.text {
			font-size: 14px;
			margin-left: 10px;
		}

		.icon {
			margin-top: 4px;
			width: 90rpx;
			height: 40px;
			font-size: 30px;
			line-height: 40px;
			text-align: center;
		}

		.icon-iconfontscan {
			/* 添加根据字体图标库的特定样式，如果需要 */
		}

		.nestSituation {
			margin: 5px 0;
			margin-left: 25rpx;
			width: 700rpx;
			height: 130px;
			background-color: #34d762;
		}

		.currentNest {
			height: 43px;
		}

		.currentNest-text {
			width: 125rpx;
			display: block;
			position: relative;
			left: 70rpx;
			top: -58rpx;
			font-size: 13px;
		}

		.views {
			display: flex;
			flex-direction: row;
			flex-wrap: nowrap;
			justify-content: space-around;
		}

		.views-container {
			/* border: 1px solid; */
			border-radius: 5%;
			width: 110px;
			height: 60px;
			background-color: white;
		}

		.views-func {
			font-size: 14px;
			width: 77rpx;
			position: relative;
			left: 20rpx;
			top: 30rpx;
		}

		.views-func-detail {
			font-size: 9px;
			width: 110rpx;
			position: relative;
			left: 20rpx;
			top: 33rpx;
		}

		.bird-image {
			position: relative;
			left: 25rpx;
			top: 25rpx;
			width: 700rpx;
			height: 535rpx;
			display: inline-block;
			box-sizing: border-box;
			border-radius: 5%;
		}
	</style>