<template>
  <div class="box" :style="{'height':(this.$store.state.windowHeight+15)+'px'}">
	<sacle-box>
		<div class="dataTop">
			<img  src="../assets/images/topImage.png"/>
			<div class="dateFlex">
				<div>{{ nowDate }}</div>
				<div>{{ nowTime }}</div>
				<div>{{ nowWeek }}</div>
			</div>
		</div>
		<div class="dataFlex">
			<div class="dataLift">
				<left-child1></left-child1>
				<left-child2></left-child2>
				<left-child3></left-child3>
			</div>
			<div class="dataCenter">
				<center-child></center-child>
			</div>
			<div class="dataRight">
				<right-child1></right-child1>
				<right-child2></right-child2>
				<right-child3 :nowDate="nowDate"></right-child3>
			</div>
		</div>
	</sacle-box>
  </div>
</template>

<script>
import sacleBox from '../components/SacleBox.vue'
import leftChild1 from '../components/leftChild1.vue'
import leftChild2 from '../components/leftChild2.vue'
import leftChild3 from '../components/leftChild3.vue'
import centerChild from '../components/centerChild.vue'
import rightChild1 from '../components/rightChild1.vue'
import rightChild2 from '../components/rightChild2.vue'
import rightChild3 from '../components/rightChild3.vue'
export default {
	components:{
		sacleBox,
		leftChild1,
		leftChild2,
		leftChild3,
		centerChild,
		rightChild1,
		rightChild2,
		rightChild3
	},
  data(){
	  return{
			nowDate:'',//日期
			nowTime:'',//时间
			nowWeek:'',//星期
			timer:'',//计时器
	  }
  },
  created() {
  	this.$store.state.windowHeight = document.documentElement.clientHeight
		clearInterval(this.timer);
		this.timer = setInterval(() => {
			this.setNowTimes()
		}, 1000)
  },
	mounted() {
		window.addEventListener("keydown", this.KeyDown, true); 
	},
	destroyed() {
		clearInterval(this.timer);
	},
	methods:{
		KeyDown(event) {
			let that = this
			if(event.code == 'F11'){
				location.reload()
			}
		 },
		setNowTimes() {
			let myDate = new Date()
			let wk = myDate.getDay()
			let yy = String(myDate.getFullYear())
			let mm = myDate.getMonth() + 1
			let dd = String(myDate.getDate() < 10 ? '0' + myDate.getDate() : myDate.getDate())
			let hou = String(myDate.getHours() < 10 ? '0' + myDate.getHours() : myDate.getHours())
			let min = String(myDate.getMinutes() < 10 ? '0' + myDate.getMinutes() : myDate.getMinutes())
			let sec = String(myDate.getSeconds() < 10 ? '0' + myDate.getSeconds() : myDate.getSeconds())
			let weeks = ['星期日', '星期一', '星期二', '星期三', '星期四', '星期五', '星期六']
			let week = weeks[wk]
			this.nowDate = yy + '-' + mm + '-' + dd
			this.nowTime = hou + ':' + min + ':' + sec
			this.nowWeek = week
		}
	}
}
</script>
<style scoped lang="scss">
	.box{
		background-image: url(../assets/images/backgroundImage.png);
		background-size: 100%;
		padding: 0;
		margin: 0;
	}
	.dataTop{
		margin-bottom: 13px;
		width: 100%;
		position: relative;
		img{
			width: 1472px;
			height: 95px;
			margin: auto;
			display: block;
		}
		.dateFlex{
			width: 273px;
			display: flex;
			align-items: center;
			justify-content: space-between;
			font-size: 18px;
			color: #2AA7D3;
			position: absolute;
			top: 34px;
			right: 40px;
		}
	}
	.dataFlex{
		display: flex;
		align-items: flex-start;
		justify-content: space-between;
		padding: 0 23px 30px 18px;
		box-sizing: border-box;
		.dataLift{
			width: 496px;
		}
		.dataRight{
			width: 496px;
		}
		.dataCenter{
			width: 933px;
		}
	}
</style>
