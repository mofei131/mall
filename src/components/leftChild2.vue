<template>
	<div class="left2Box">
		<div class="listFlex">
			<div class="left1">
				<img  src="../assets/images/left2Icon.png"/>
				<div class="leftchild1">
					<div class="left1Top">今日上市量</div>
					<div class="left1Bot">
						<div class="left2">220.35</div>
						<div class="right2">万公斤</div>
					</div>
				</div>
			</div>
			<div class="right1">
				<div class="right1Top">
					<div class="left2">周同比</div>
					<div class="right2">↑3.24%</div>
				</div>
				<div class="right1Top">
					<div class="left2">周环比</div>
					<div class="right2">↑2.69%</div>
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
	.left2Box{
		width: 496px;
		height: 205px;
		background-image: url(../assets/images/leftImage2.png);
		background-size: 100%;
		background-repeat: no-repeat;
		margin-bottom: 30px;
	}
	.listFlex{
		display: flex;
		align-items: center;
		justify-content: space-around;
		width: 496px;
		padding-top: 64px;
		box-sizing: border-box;
		.left1{
			display: flex;
			align-items: center;
			img{
				width: 77px;
				height: 84px;
				margin-right: 13px;
			}
			.leftchild1{
				display: flex;
				flex-direction: column;
				justify-content: space-around;
				height: 84px;
				.left1Top{
					font-size: 18px;
					font-weight: 600;
					color: #FEFFFF;
				}
				.left1Bot{
					display: flex;
					align-items: flex-end;
					.left2{
						font-size: 32px;
						font-weight: bold;
						color: #EDB138;
						margin-right: 5px;
					}
					.right2{
						font-size: 18px;
						color: #EDB138;
					}
				}
			}
		}
		.right1{
			display: flex;
			flex-direction: column;
			justify-content: space-around;
			height: 84px;
			.right1Top{
				display: flex;
				align-items: center;
				justify-content: space-between;
				width: 136px;
				.left2{
					font-size: 18px;
					font-weight: 400;
					color: #FEFFFF;
				}
				.right2{
					font-size: 18px;
					font-weight: 400;
					color: #FC0808;
				}
			}
		}
	}
</style>