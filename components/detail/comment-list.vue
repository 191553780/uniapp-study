<template>
	<view class="uni-comment-list animated fast fadeIn" 
		:class="{'u-comment-list-child': item.fid > 0}"
	>
		<view class="uni-comment-face">
			<image :src="item.userpic" mode="widthFix"></image>
		</view>
		<view class="uni-comment-body">
			<view class="uni-comment-top">
				<text>{{item.username}}</text>
			</view>
			<view class="uni-comment-content">{{item.data}}</view>
			<view class="uni-comment-date">
				<view>{{item.time}}</view>
			</view>
		</view>
	</view>
</template>

<script>
export default {
	props: {
		item: Object,
		index: Number
	}
}
</script>

<style lang="scss" scoped>
.u-comment-list-child {
		padding: 20rpx;
		background: #f4f4f4;
		border-bottom: 1rpx solid #eee;
		box-sizing: border-box;
		margin: 0;
		margin-left: 70rpx;
		width: auto;
	}
</style>
