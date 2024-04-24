# 注意： 使用前需要导入 cc-excelOne 、cc-excelTwo两个插件


#### 使用方法 
```使用方法
	
<!-- cc-excelOne使用方法 title：标题  value：结果值 -->
<cc-excelOne title="企业规模" :value="infoData.qygm"></cc-excelOne>

<!-- cc-excelTwo使用方法 title：标题  titleTwo：右边标题 value：结果值 valueTwo：右边结果值 -->
<cc-excelTwo title="组织机构代码" titleTwo="高企证书编号" :value="infoData.comCode"
	:valueTwo="infoData.certificateNo"></cc-excelTwo>


```

#### HTML代码实现部分
```html
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
				<cc-excelOne title="经营范围" :value="infoData.businessScope"></cc-excelOne>



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
```