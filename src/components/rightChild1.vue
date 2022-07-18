<template>
	<div class="right1Box">
		<div class="carBox">
			<div class="carOne">
				<img src="../assets/images/carIcon.png"/>
				<div class="carSum">
					<div class="carTop">195</div>
					<div class="carBot">进场车辆总数</div>
				</div>
			</div>
			<div class="carOne">
				<img src="../assets/images/carIcon.png"/>
				<div class="carSum">
					<div class="carTop">133</div>
					<div class="carBot">当前场内车辆总数</div>
				</div>
			</div>
			<div class="carOne">
				<img src="../assets/images/carIcon.png"/>
				<div class="carSum">
					<div class="carTop">62</div>
					<div class="carBot">出场车辆总数</div>
				</div>
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
	.right1Box{
		width: 496px;
		height: 155px;
		background-image: url(../assets/images/rightImage1.png);
		background-repeat: no-repeat;
		background-size: 100%;
		margin-bottom: 29px;
		.carBox{
			display: flex;
			align-items: center;
			justify-content: space-around;
			padding-top: 54px;
			.carOne{
				display: flex;
				align-items: center;
				img{
					width: 36px;
					height: 28px;
					margin-right: 17px;
				}
				.carSum{
					display: flex;
					flex-direction: column;
					justify-content: space-between;
					.carTop{
						font-size: 32px;
						font-weight: bold;
						color: #F8B62D;
					}
					.carBot{
						width: 90px;
						height: 31px;
						font-size: 14px;
						font-weight: normal;
						color: #00CAFF;
					}
				}
			}
		}
	}
</style>