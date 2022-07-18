<template>
	<div class="centerBox">
		<div class="topFlex">
			<div class="topOne">
				<div class="top1">426亩</div>
				<div class="top2">占地面积</div>
			</div>
			<div class="topOne">
				<div class="top1">38万平方</div>
				<div class="top2">建筑面积</div>
			</div>
			<div class="topOne">
				<div class="top1">6个</div>
				<div class="top2">经营区域</div>
			</div>
			<div class="topOne">
				<div class="top1">480+</div>
				<div class="top2">固定用户</div>
			</div>
			<div class="topOne">
				<div class="top1">1900左右</div>
				<div class="top2">固定摊位</div>
			</div>
			<div class="topOne">
				<div class="top1">蔬菜50+</div>
				<div class="top2">交易品种</div>
			</div>
			<div class="topOne">
				<div class="top1">200+</div>
				<div class="top2">交易车辆</div>
			</div>
			<div class="topOne">
				<div class="top1">2万+</div>
				<div class="top2">日人流量</div>
			</div>
			<div class="topOne">
				<div class="top1">44万吨(年)</div>
				<div class="top2">市场总上市量</div>
			</div>
			<div class="topOne">
				<div class="top1">46亿(年)</div>
				<div class="top2">市场总成交额</div>
			</div>
		</div>
		<div class="fontBox">
			衢州农商城创办于2013年，系北京市国资委旗下企业北控集团通过其香港上市子公司北京建设在衢投资建设，占地面积426亩，总投资12亿人民币，建筑面积38万平方米。项目分为蔬菜交易区、水果交易区、干货副食交易区、水产冻品交易区、早市交易区、冷库仓储区及商业配套区，是辐射浙、闵、赣、皖四省边际的大型农产品批发市场。
		</div>
		<img class="lastImage" src="../assets/images/market.jpg" alt="">
	</div>
</template>

<script>
	export default{
		data(){
			return{
				
			}
		}
	}
</script>

<style scoped lang="scss">
	.centerBox{
		width: 933px;
		height: 958px;
		background-image: url(../assets/images/centerImage.png);
		background-size: 100%;
		background-repeat: no-repeat;
		padding: 52px 31px 39px 33px;
		box-sizing: border-box;
		.topFlex{
			display: flex;
			align-items: center;
			justify-content: space-between;
			flex-wrap: wrap;
			.topOne{
				background-color: rgba(14,54,142,0.3);
				width: 159px;
				height: 100px;
				display: flex;
				flex-direction: column;
				align-items: center;
				justify-content: space-around;
				margin-bottom: 20px;
				padding: 15px 0;
				box-sizing: border-box;
				.top1{
					font-size: 18px;
					font-weight: 600;
					color: #F8B62D;
				}
				.top2{
					font-size: 16px;
					font-weight: 600;
					color: #D4EAF6;
				}
			}
		}
		.fontBox{
			width: 849px;
			height: 186px;
			font-size: 26px;
			font-weight: 400;
			color: #FFFFFF;
			line-height: 40px;
			padding-top: 6px;
			margin: auto;
			margin-bottom: 26px;
		}
		.lastImage{
			width: 864px;
			height: 409px;
			margin: auto;
			display: block;
		}
	}
</style>