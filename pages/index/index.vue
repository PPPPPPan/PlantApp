<template>
	<div class="index-section">
		<div class="index-box">
			<image class="index-img"
				src="https://panshijie-plantapp-1255388042.cos.ap-guangzhou.myqcloud.com/index-img.png"
				alt="" mode="widthFix" lazy-load="true">
				<button class="index-btn" type="default" size="mini">开启邂逅之旅</button>
				<template>
					<van-dialog id="van-dialog" />
				</template>
		</div>
	</div>
</template>

<script>
	import Dialog from '../../wxcomponents/vant/dist/dialog/dialog'
	export default {
		data() {
			return {};
		},
		onShow() {
			Dialog.confirm({
					title: '植悟 V2.0',
					message: '弹窗内容',
				})
				.then(() => {
					// on confirm
				})
				.catch(() => {
					// on cancel
				});
		}
	}
</script>

<style lang="scss">
	.index-section {
		height: 100vh;
		display: flex;
		flex-direction: column;
		justify-content: center;

		.index-box {
			text-align: center;

			.index-img {
				width: 550upx;
				height: 841upx;
			}

			.index-btn {
				width: 300upx;
				height: 50upx;
				line-height: 50upx;
				font-size: 28upx;
				color: $pa-text-primary;
				background-color: $pa-color-primary;
				margin-top: 100upx;
			}
		}
	}
</style>
