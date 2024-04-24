<template>
	<view class="content">

		<div style="padding: 0px 12px;background: white;">

			<div class="topView" style="">
				<!-- 第一行 -->
				<cc-excelOne title="企业曾用名" :value="infoData.comNameOld"></cc-excelOne>

				<!-- 第二行 -->
				<cc-excelOne title="企业规模" :value="infoData.qygm"></cc-excelOne>



				<!-- 第三行 -->
				<cc-excelTwo title="组织机构代码" titleTwo="高企证书编号" :value="infoData.comCode"
					:valueTwo="infoData.certificateNo"></cc-excelTwo>


				<!-- 第四行 -->
				<cc-excelTwo title="注册时间" titleTwo="注册资本" value="" valueTwo=""></cc-excelTwo>

				<!-- 第五行 -->
				<cc-excelTwo title="所属地市" titleTwo="所属行政区域" value="" valueTwo=""></cc-excelTwo>

				<!-- 第六行 -->
				<cc-excelOne title="单位地址" :value="infoData.address"></cc-excelOne>

				<!-- 第七行 -->
				<cc-excelTwo title="行业类型" titleTwo="行业门类" value="" valueTwo=""></cc-excelTwo>

				<!-- 第八行 -->
				<cc-excelTwo title="是否高新技术企业" titleTwo="是否负面清单" value="是" valueTwo="否"></cc-excelTwo>


				<!-- 第九行 -->
				<cc-excelThr title="所在省" titleTwo="所在市" titleThr="所在区" value="广东省" valueTwo="广州市"
					valueThr="天河区"></cc-excelThr>

				<!-- 第十行 -->
				<cc-excelFour title="所属行业" titleTwo="所属行业" titleThr="所属行业" titleFour="所属行业" value="金融" valueTwo="互联网"
					valueThr="人工智能" valueFour="VR/AR"></cc-excelFour>



			</div>
		</div>


	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				infoData: {}
			}
		},
		onLoad() {

		},
		methods: {


		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		width: 100%;

	}

	.topView {
		margin-left: 0px;
		width: 100%;
		margin-bottom: 80px;
		margin-top: 16px;

		border-top: 1px solid #e9e9e9;
		border-right: 1px solid #e9e9e9;



	}
</style>