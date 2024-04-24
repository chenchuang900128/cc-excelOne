<template>
	<view>
		<!-- 一行一列 -->
		<view class="rowCell">

			<view style="display: flex;width:50%">

				<view class="baseInfoTwoTitle">
					{{title}}
				</view>
				<view class="baseInfoTwo">
					{{ ZJNoEmptyString(value) }}
				</view>

			</view>


			<view style="display: flex; width:50%">

				<view class="baseInfoTwoTitle">
					{{titleTwo}}
				</view>
				<view class="baseInfoTwo">
					{{ ZJNoEmptyString(valueTwo)}}
				</view>


			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props: {

			title: {
				type: String,
				default: ''
			},
			value: {
				type: [String, Number],
				default: ''
			},
			titleTwo: {
				type: String,
				default: ''
			},
			valueTwo: {
				type: [String, Number],
				default: ''
			}

		},
		data() {
			return {

			}
		},

		computed: {

		},
		methods: {

			ZJNoEmptyString(obj) {

				let str = '--';
				if (typeof(obj) == "undefined" || (obj) === null || (obj) === '') {
					return str;
				}
				return obj + '';
			}

		}
	}
</script>


<style>
	/* 每行样式 */
	.rowCell {

		display: flex;
		border-bottom: 1px solid #e9e9e9;
		background: #FCFCFC;
	}


	/* 一行两列标题样式 */
	.baseInfoTwoTitle {
		font-size: 13px;
		color: #666666;
		line-height: 40px;
		height: 40px;
		width: 100px;
		background: #F2F9FC;
		text-align: center;

		border-left: 1px solid #e9e9e9;
		border-right: 1px solid #e9e9e9;

	}

	/* 一行两列内容样式 */
	.baseInfoTwo {
		font-size: 14px;
		color: #303236;
		line-height: 40px;
		height: 40px;
		width: auto;
		padding: 0px 20px;
		font-weight: 500;
		font-family: PingFangSC, PingFangSC;


	}
</style>