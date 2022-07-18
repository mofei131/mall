<template>
	<div class="right2Box">
		<div class="right2Flex">
			<div>
				<div id="ring_chart1" style="width: 100px;height: 100px;"></div>
				<div class="fontText">停车位总量(个)</div>
			</div>
			<div>
				<div id="ring_chart2" style="width: 100px;height: 100px;"></div>
				<div class="fontText">剩余停车位(个)</div>
			</div>
			<div>
				<div id="ring_chart3" style="width: 100px;height: 100px;"></div>
				<div class="fontText">空余车位占比</div>
			</div>
		</div>
	</div>
</template>

<script>
	export default{
		data(){
			return{
				
			}
		},
		mounted() {
			this.drawChart()
			this.drawChart2()
			this.drawChart3()
		},
		methods:{
			drawChart(){
				let Chart = this.$echarts.init(document.getElementById('ring_chart1'))
				let option = {
					title: {
					    text: '260',
					    left: 'center',
					    top: 40,
					    textStyle:{
					      color:'#E73851',
								fontSize:24
					    }
					  },
					  visualMap: {
					    show: false,
					  },
					  series: [
					    {
					      type: 'pie',
					      //环形显示饼状图，实际上显示的是50-80之间的部分
					      //上限不建议设置为100，echarts自带动画效果，设置为100动画效果很丑
					      radius: ['80%', '90%'],
					      center: ['50%', '50%'],
					      data: [
					      //itemSyle是单项的背景颜色设置。
					        { value: 0, itemStyle: { color: '#041c59' } },
					        { value: 100, itemStyle: { color: '#E73851' } },
					      ],
					      label: {
					        //将视觉引导图关闭
					        show: false,
					      },
					      itemStyle:{
					      	//设置的是每项之间的留白
					        borderWidth:0,
					        borderColor:'#fff'
					      },
					      // 初始化echarts的动画效果
					      animationType: 'scale',
					      animationEasing: 'elasticOut',
					      animationDelay: function (idx) {
					        return Math.random() * 200;
					      }
					    }
					  ],
					}
				Chart.setOption(option)
			},
			drawChart2(){
				let Chart = this.$echarts.init(document.getElementById('ring_chart2'))
				let option = {
					title: {
					    text: '86',
					    left: 'center',
					    top: 40,
					    textStyle:{
					      color:'#D1B55D',
								fontSize:24,
					    }
					  },
					  visualMap: {
					    show: false,
					  },
					  series: [
					    {
					      type: 'pie',
					      //环形显示饼状图，实际上显示的是50-80之间的部分
					      //上限不建议设置为100，echarts自带动画效果，设置为100动画效果很丑
					      radius: ['80%', '90%'],
					      center: ['50%', '50%'],
					      data: [   
					      //itemSyle是单项的背景颜色设置。
					        { value: 90, itemStyle: { color: '#041c59' } },
					        { value: 10, itemStyle: { color: '#D1B55D' } },
					      ],
					      label: {
					        //将视觉引导图关闭
					        show: false,
					      },
					      itemStyle:{
					      	//设置的是每项之间的留白
					        borderWidth:0,
					        borderColor:'#fff'
					      },
					      // 初始化echarts的动画效果
					      animationType: 'scale',
					      animationEasing: 'elasticOut',
					      animationDelay: function (idx) {
					        return Math.random() * 200;
					      }
					    }
					  ],
					}
				Chart.setOption(option)
			},
			drawChart3(){
				let Chart = this.$echarts.init(document.getElementById('ring_chart3'))
				let option = {
					title: {
					    text: '66.9%',
					    left: 'center',
					    top: 40,
					    textStyle:{
					      color:'#80C9C2',
								fontSize:24
					    }
					  },
					  visualMap: {
					    show: false,
					  },
					  series: [
					    {
					      type: 'pie',
					      //环形显示饼状图，实际上显示的是50-80之间的部分
					      //上限不建议设置为100，echarts自带动画效果，设置为100动画效果很丑
					      radius: ['80%', '90%'],
					      center: ['50%', '50%'],
					      data: [   
					      //itemSyle是单项的背景颜色设置。
					        { value: 23, itemStyle: { color: '#041c59' } },
					        { value: 67, itemStyle: { color: '#80C9C2' } },
					      ],
					      label: {
					        //将视觉引导图关闭
					        show: false,
					      },
					      itemStyle:{
					      	//设置的是每项之间的留白
					        borderWidth:0,
					        borderColor:'#fff'
					      },
					      // 初始化echarts的动画效果
					      animationType: 'scale',
					      animationEasing: 'elasticOut',
					      animationDelay: function (idx) {
					        return Math.random() * 200;
					      }
					    }
					  ],
					}
				Chart.setOption(option)
			}
		}
	}
</script>

<style scoped lang="scss">
	.right2Box{
		width: 496px;
		height: 186px;
		background-image: url(../assets/images/rightImage2.png);
		background-repeat: no-repeat;
		background-size: 100%;
		margin-bottom: 29px;
	}
	.right2Flex{
		display: flex;
		align-items: center;
		justify-content: space-around;
		padding-top: 37px;
		.fontText{
			font-size: 14px;
			font-weight: 400;
			color: #D4EAF6;
		}
	}
</style>