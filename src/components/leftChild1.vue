<template>
	<div class="leftChild1Box">
		<div class="treeFelx">
			<div class="leftOne">
				<div class="left1Num">1353</div>
				<img src="../assets/images/left1Icon.png"/>
				<div class="pop">累计进场人数</div>
			</div>
			<div class="leftOne">
				<div class="left1Num">821</div>
				<img src="../assets/images/left1Icon.png"/>
				<div class="pop">当前场内人数</div>
			</div>
			<div class="leftOne">
				<div class="left1Num">532</div>
				<img src="../assets/images/left1Icon.png"/>
				<div class="pop">累计出场人数</div>
			</div>
		</div>
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
	.leftChild1Box{
		width: 496px;
		height: 204px;
		margin-bottom: 29px;
		background-image: url(../assets/images/leftImage1.png);
		background-size: 100%;
		background-repeat: no-repeat;
	}
	.treeFelx{
		width: 496px;
		display: flex;
		align-items: center;
		justify-content: space-around;
		padding-top: 46px;
		.leftOne{
			.left1Num{
				font-size: 32px;
				font-weight: bold;
				color: #EDB138;
				text-align: center;
			}
			img{
				width: 80px;
				height: 80px;
				margin: auto;
				display: block;
			}
			.pop{
				font-size: 16px;
				font-weight: 600;
				color: #FFFFFF;
				text-align: center;
			}
		}
	}
</style>