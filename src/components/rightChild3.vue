<template>
	<div class="right3Box">
		<div class="swiperTop">
			<div>车牌</div>
			<div>车型</div>
			<div>通道</div>
			<div>进场时间</div>
			<div>出场时间</div>
		</div>
		<div class="swiper-container">
			<div class="swiper-wrapper">
				<div class="swiper-slide" v-for="(item,index) in dataList" :key="index">
					<div class="slideChide">{{item.name}}</div>
					<div class="slideChide">{{item.weight}}</div>
					<div class="slideChide">{{item.price}}</div>
					<div class="slideChide">{{nowDate}}</div>
					<div class="slideChide">{{item.status == 1? nowDate : ''}}</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
	import Swiper from 'swiper'
	export default{
		props:['nowDate','nowTime'],
		data(){
			return{
				dataList:[
					{name:'浙A78***',weight:'4.2米厢货',price:'货车出口',inDate:'2022-7-17',outDate:'2022-7-18',status:2},
					{name:'浙A12***',weight:'4.2米厢货',price:'货车出口',inDate:'2022-7-16',outDate:'2022-7-18',status:2},
					{name:'浙B54***',weight:'6.2米厢货',price:'货车入口',inDate:'2022-7-18',outDate:'',status:1},
					{name:'京A76***',weight:'7.2米厢货',price:'货车入口',inDate:'2022-7-18',outDate:'',status:1},
					{name:'鲁A56***',weight:'小轿车',price:'小轿车出口',inDate:'2022-7-18',outDate:'2022-7-18',status:1},
					{name:'豫A54***',weight:'6.2米厢货',price:'货车出口',inDate:'2022-7-18',outDate:'2022-7-18',status:1},
					{name:'鲁G65***',weight:'7.2米厢货',price:'货车出口',inDate:'2022-7-18',outDate:'2022-7-18',status:1},
					{name:'浙H56***',weight:'小轿车',price:'小轿车入口',inDate:'2022-7-18',outDate:'',status:1},
					{name:'浙H98***',weight:'7.2米厢货',price:'货车入口',inDate:'2022-7-18',outDate:'',status:1},
					{name:'浙H43***',weight:'4.2米厢货',price:'货车出口',inDate:'2022-7-16',outDate:'2022-7-18',status:2},
					{name:'浙H98***',weight:'6.2米厢货',price:'货车出口',inDate:'2022-7-18',outDate:'2022-7-18',status:1},
					{name:'浙H17***',weight:'4.2米厢货',price:'货车入口',inDate:'2022-7-18',outDate:'',status:1},
					{name:'豫R78***',weight:'7.2米厢货',price:'货车出口',inDate:'2022-7-16',outDate:'2022-7-18',status:2},
					{name:'浙A78***',weight:'4.2米厢货',price:'货车出口',inDate:'2022-7-17',outDate:'2022-7-18',status:2},
					{name:'浙A12***',weight:'4.2米厢货',price:'货车出口',inDate:'2022-7-16',outDate:'2022-7-18',status:2},
					{name:'浙B54***',weight:'6.2米厢货',price:'货车入口',inDate:'2022-7-18',outDate:'',status:1},
					{name:'京A76***',weight:'7.2米厢货',price:'货车入口',inDate:'2022-7-18',outDate:'',status:1},
					{name:'鲁A56***',weight:'小轿车',price:'小轿车出口',inDate:'2022-7-18',outDate:'2022-7-18',status:1},
					{name:'豫A54***',weight:'6.2米厢货',price:'货车出口',inDate:'2022-7-18',outDate:'2022-7-18',status:1},
					{name:'鲁G65***',weight:'7.2米厢货',price:'货车出口',inDate:'2022-7-18',outDate:'2022-7-18',status:1},
					{name:'浙H56***',weight:'小轿车',price:'小轿车入口',inDate:'2022-7-18',outDate:'',status:1},
					{name:'浙H98***',weight:'7.2米厢货',price:'货车入口',inDate:'2022-7-18',outDate:'',status:1},
					{name:'浙H43***',weight:'4.2米厢货',price:'货车出口',inDate:'2022-7-16',outDate:'2022-7-18',status:2},
					{name:'浙H98***',weight:'6.2米厢货',price:'货车出口',inDate:'2022-7-18',outDate:'2022-7-18',status:1},
					{name:'浙H17***',weight:'4.2米厢货',price:'货车入口',inDate:'2022-7-18',outDate:'',status:1},
					{name:'豫R78***',weight:'7.2米厢货',price:'货车出口',inDate:'2022-7-16',outDate:'2022-7-18',status:2},
				],
			}
		},
		mounted() {
			let swiper = new Swiper('.swiper-container', {
				direction: 'vertical',
				loop: true,
				slidesPerView:14,
				speed:1000,
				autoplay: {
					delay: 3000,
					disableOnInteraction: false, 
				},
				observer:true,
				observeParents:true,
				onSlideChangeEnd: function(swiper){
				//更新Swiper，这个方法包含了updateContainerSize，updateSlidesSize，updateProgress，updatePagination，updateClasses方法。也就是数据改变是重新初始化一次swiper；
				  swiper.update();
				//重新对需要循环的slide个数进行计算，当你改变了slidesPerView参数时需要用到，需要自动轮播的时候必须要加上；
				  swiper.reLoop();
				//重新开始自动切换；
				  swiper.startAutoplay();
				},
			});
		}
	}
</script>

<style scoped lang="scss">
	@import url("../../node_modules/swiper/dist/css/swiper.min.css");
	.right3Box{
		width: 497px;
		height: 557px;
		background-image: url(../assets/images/rightImage3.png);
		background-size: 100%;
		background-repeat: no-repeat;
		padding: 49px 20px 38px 19px;
		box-sizing: border-box;
	}
	.swiperTop{
		width: 458px;
		height: 37px;
		background-color: rgba(241,241,241,0.06);
		display: flex;
		align-items: center;
		justify-content: space-between;
		div{
			display: flex;
			align-items: center;
			justify-content: center;
			width: 91px;
			font-size: 16px;
			font-weight: normal;
			color: #06B2F1;
		}
	}
	.swiper-container{
		height: 433px;
		width: 458px;
		.swiper-wrapper{
			height: 433px;
			width: 458px;
		}
		.swiper-slide{
			width: 458px;
			display: flex;
			align-items: center;
			justify-content: space-between;
			.slideChide{
				font-size: 14px;
				font-weight: 500;
				color: #D4EAF6;
				width: 91px;
				text-align: center;
			}
		}
		.swiper-slide:nth-child(2n){
			background-color: rgba(241,241,241,0.06);
		}
	}
</style>