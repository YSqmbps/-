<template>
	<view>
		<view class="head">
			
			<view class="top-func">
				<view class="icon iconfont icon-iconfontscan" style="font-size: 30px; position: relative; left: 25rpx; top: 10rpx;"></view>
				<view class="icon iconfont icon-shezhi" style="font-size: 30px; position: relative; left: -25rpx; top: 10rpx;"></view>
			</view>
			
			<view class="avatar-container">
				<view>
					<img src="@/static/pexels-ant-armada-322180244-27400950(1).png" alt="" class="avatar"/>
				</view>
			</view>
			
			<view>
				<text class="username">昵称</text>
			</view>
			
		</view>
		
		<view class="middle">
			<view class="mid-func">
				<view class="icon iconfont icon-fenxiangdingqijieshao" style="position: relative; top: -10rpx;"></view>
				<view class="small-func">产品介绍</view>
				<view class="icon iconfont icon-youjiantou"></view>
			</view>
			
			<view class="mid-func">
				<view class="icon iconfont icon-gerenxinxi" style="position: relative; top: -10rpx;"></view>
				<view class="small-func">个人信息</view>
				<view class="icon iconfont icon-youjiantou"></view>
			</view>
			
			<view class="mid-func">
				<view class="icon iconfont icon-yijianfankui" style="position: relative; top: -10rpx; left: -10rpx;"></view>
				<view class="small-func" style="left: -215rpx;">意见反馈</view>
				<view class="icon iconfont icon-youjiantou"></view>
			</view>
			
			<view class="mid-func">
				<view class="icon iconfont icon-tuichu" style="position: relative; top: -10rpx;"></view>
				<view class="small-func">点击退出</view>
				<view class="icon iconfont icon-youjiantou"></view>
			</view>
		</view>
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

<style>
	.head {
		width: 750rpx;
		height: 250rpx;
		background-color: #74E868;
	}
	
	.top-func {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		top: -2rpx;
		height: 72rpx;
	}
	.avatar {
		position: relative;
		left: 316rpx;
		width: 120rpx;
		height: 120rpx;
		top: -24rpx;
		border-radius: 50%;
	}
	.username {
		position: relative;
		left: 345rpx;
		top: -20rpx;
	}
	.middle {
		display: flex;
		flex-direction: column;
		margin: 20px;
		padding: 15px 0;
		width: 350px;
		height: 250px;
		background-color: #F0F8FF;
		border-radius: 5%;
		
	}
	.mid-func {
		margin: 15px;
		border-bottom: 1px solid;
		display: flex;
		flex-direction: row;
		justify-content: space-between;
	}
	.icon .iconfont {
		position: relative;
		top: -10rpx;
	}
	.small-func {
		position: relative;
		left: -200rpx;
		top: -18rpx;
	}
	.icon .iconfont .icon-youjiantou {
		position: relative;
		top: -8rpx;
	}
</style>
