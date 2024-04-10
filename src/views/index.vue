<template>
  <div class="app-container home" style="padding: 0;margin: 0;">
    <div  class="div-layout" >
		<el-row>
			<div style="background-color: #212121;border-radius: 15px">
				<el-row>
					<el-col :span="6" style="color: white;font-size: 16px;font-weight: 350;padding-top: 15px;padding-bottom: 15px;">
						<span style="text-shadow: 0 0 0.3rem #00d8ff;font-size: 25px;font-weight: 550; letter-spacing: 10px;padding-left: 40px;">校园安防指挥平台</span>
					</el-col>
					<el-col :span="6" style="color: white;padding-top: 25px;">
						<el-row style="padding-left: 0px;">
							<router-link to="/index">
								<el-col :span="7">
									<span style="font-size: 16px;font-weight: 550;">数据概览</span>
								</el-col>
							</router-link>
							<router-link to="/eme">
								<el-col :span="8">
									<span style="font-size: 16px;font-weight: 550;">应急指挥</span>
								</el-col>
							</router-link>
						</el-row>
					</el-col>
					<el-col :span="12" style="color: white;font-size: 16px;font-weight: 350;padding-top: 30px;padding-left: 300px;">
						<el-row >
							<el-col :span="16" style="padding-left:100px">
								<div><span>{{newTime}} </span></div>
							</el-col>
							<el-col :span="5">
								<i class="el-icon-user-solid"></i>
								<span>管理员</span>
							</el-col>
							<el-col :span="3">
								<i class="el-icon-switch-button"></i>
							</el-col>
						</el-row>
					</el-col>
				</el-row>
			</div>
		</el-row>
		<el-row>
			<el-col :span="6" style="padding-left: 20px;padding-top: 30px;">
				<el-row style="background-color: rgba(22, 31, 38, 0.7);">
					<el-row>
						<div class="titlebox" >
							<span style="font-size: 20px;font-weight:450;color:white;padding-left: 20px;    text-shadow: 0.3rem 0 0.3rem #c1faff;">告警监测</span>
						</div>
					</el-row>
					<el-row>
						<div style="display: flex;padding-top: 15px;">
							<span style="color: white;font-size: 15px;font-weight: 500;padding-left: 10px;">警情信号</span>
							<div style="padding-left: 50px;"></div>
							<div class="breathe-zct"></div>
							<span style="color: white;font-size: 13px;font-weight: 500;padding-left: 5px;padding-top: 5px;">正常</span>
							<div style="padding-left: 30px;"></div>
							<div class="breathe-yct"></div>
							<span style="color: white;font-size: 13px;font-weight: 500;padding-left: 5px;padding-top: 5px;">告警</span>
						</div>
					</el-row>
					<el-row style="zoom:0.9;padding-top: 15px;padding-bottom: 20px;">
						<el-col :span="6" style="padding-left: 10px;">
							<el-row style="padding-left: 20px;">
								<div id="dx" class="breathe-zc breathe-zct " style="zoom:0.8"></div>
							</el-row>
							<el-row>
								<span style="color: white;font-size: 15px;font-weight: 500;">人员告警</span>
							</el-row>
						</el-col>
						<el-col :span="6" style="padding-left: 10px;">
							<el-row style="padding-left: 20px;"> 
								<div id="dx" class="breathe-zc breathe-zct " style="zoom:0.8"></div>
							</el-row>
							<el-row>
								<span style="color: white;font-size: 15px;font-weight: 500;">消防告警</span>
							</el-row>
						</el-col>
						<el-col :span="6" style="padding-left: 10px;">
							<el-row style="padding-left: 20px;">
								<div id="dx" class="breathe-zc breathe-zct " style="zoom:0.8"></div>
							</el-row>
							<el-row>
								<span style="color: white;font-size: 15px;font-weight: 500;">交通告警</span>
							</el-row>
						</el-col>
						<el-col :span="6" style="padding-left: 10px;">
							<el-row style="padding-left: 20px;">
								<div id="dx" class="breathe-zc breathe-zct " style="zoom:0.8"></div>
							</el-row>
							<el-row>
								<span style="color: white;font-size: 15px;font-weight: 500;">设备告警</span>
							</el-row>
						</el-col>
					</el-row>
				</el-row>
				
				
				<el-row>
					<div style="padding-top: 20px;"></div>
				</el-row>
				
				<el-row style="background-color: rgba(22, 31, 38, 0.7);">
					<el-row>
						<div class="titlebox" >
							<span style="font-size: 20px;font-weight:500;color:white;padding-left: 20px;text-shadow: 0.3rem 0 0.3rem #c1faff;">消防态势</span>
						</div>
					</el-row>
					
					<el-row>
						<el-col :span="12">
							<div style="padding-left: 20px;padding-top: 10px;">
								<div class="kuang" style="color: white;height: 70px;width: 180px;">
									<div style="padding-left: 20px;">
										<el-row  style="padding-top: 10px;">
											<span style="font-size: 13px;">消防故障点</span>
										</el-row>
										<el-row style="padding-bottom: 10px;">
											<span style="font-size: 24px;color: #00deff;text-shadow: 0 0 5px #00deff;font-family: electronicFont;">8</span>
											<i class="text-d" style="font-size: 12px;color: #ff6316;">↑4.01%</i>
										</el-row>
									</div>
								</div>
							</div>
						</el-col>
						
						<el-col :span="12">
							<div style="padding-left: 20px;padding-top: 10px;">
								<div class="kuang" style="color: white;height: 70px;width: 180px;">
									<div style="padding-left: 20px;">
										<el-row  style="padding-top: 10px;">
											<span style="font-size: 13px;">消防设施总数</span>
										</el-row>
										<el-row style="padding-bottom: 10px;">
											<span style="font-size: 24px;color: #00deff;text-shadow: 0 0 5px #00deff;font-family: electronicFont;">80</span>
											<i class="text-d" style="font-size: 12px;color: #ff6316;">↑2.01%</i>
										</el-row>
									</div>
								</div>
							</div>
						</el-col>
					</el-row>
					<!-- <el-row>
						<div style="display: flex;padding-top: 15px;">
							<span style="color: white;font-size: 15px;font-weight: 500;padding-left: 10px;">消防设施</span>
						</div>
					</el-row> -->
					<el-row>
						<div class="Echarts" style="width:`180px;">
						  <div id="char6" style="width:`180px;height: 200px;"></div>
						</div>
					</el-row>
				</el-row>
				
				<el-row>
					<div style="padding-top: 20px;"></div>
				</el-row>
				
				<el-row style="background-color: rgba(22, 31, 38, 0.7);">
					<el-row>
						<div class="titlebox" >
							<span style="font-size: 20px;font-weight:500;color:white;padding-left: 20px;text-shadow: 0.3rem 0 0.3rem #c1faff;">食品卫生评分</span>
						</div>
					</el-row>
					<el-row>
						<!-- <div style="display: flex;padding-top: 15px;">
							<span style="color: white;font-size: 15px;font-weight: 500;padding-left: 10px;">评分等级</span>
						</div> -->
					</el-row>
					<el-row>
						<div class="Echarts" style="width:`180px;">
						  <div id="char7" style="width:`180px;height: 210px;"></div>
						</div>
					</el-row>
				</el-row>
			</el-col>
			
			
			<el-col :span="12" style="padding-left: 20px;padding-top: 30px;">
				<el-row style="background-color: rgba(22, 31, 38, 0.7);">
					<el-col :span="6">
						<div style="padding-left: 40px;padding-top: 10px;padding-bottom: 10px;">
							<div class="kuang5" style="color: white;height: 70px;width: 180px;">
								<div style="padding-left: 20px;">
									<el-row  style="padding-top: 10px;">
										<span style="font-size: 13px;">本周告警数</span>
									</el-row>
									<el-row style="padding-bottom: 10px;">
										<span style="font-size: 24px;color: #00deff;text-shadow: 0 0 5px #00deff;font-family: electronicFont;">30</span>
										<i class="text-d" style="font-size: 12px;color: #ff6316;">↑4.01%</i>
									</el-row>
								</div>
							</div>
						</div>
					</el-col>
					<el-col :span="6">
						<div style="padding-left: 20px;padding-top: 10px;padding-bottom: 10px;">
							<div class="kuang5" style="color: white;height: 70px;width: 180px;">
								<div style="padding-left: 20px;">
									<el-row  style="padding-top: 10px;">
										<span style="font-size: 13px;">待处理告警</span>
									</el-row>
									<el-row style="padding-bottom: 10px;">
										<span style="font-size: 24px;color: #00deff;text-shadow: 0 0 5px #00deff;font-family: electronicFont;">8</span>
										<i class="text-d" style="font-size: 12px;color: #ff6316;">↑2.01%</i>
									</el-row>
								</div>
							</div>
						</div>
					</el-col>
					<el-col :span="6">
						<div style="padding-left: 20px;padding-top: 10px;padding-bottom: 10px;">
							<div class="kuang5" style="color: white;height: 70px;width: 180px;">
								<div style="padding-left: 20px;">
									<el-row  style="padding-top: 10px;">
										<span style="font-size: 13px;">处理中告警</span>
									</el-row>
									<el-row style="padding-bottom: 10px;">
										<span style="font-size: 24px;color: #00deff;text-shadow: 0 0 5px #00deff;font-family: electronicFont;">6</span>
										<i class="text-d" style="font-size: 12px;color: #ff6316;">↑3.01%</i>
									</el-row>
								</div>
							</div>
						</div>
					</el-col>
					<el-col :span="6">
						<div style="padding-left: 20px;padding-top: 10px;padding-bottom: 10px;padding-right: 50px;">
							<div class="kuang5" style="color: white;height: 70px;width: 180px;">
								<div style="padding-left: 20px;">
									<el-row  style="padding-top: 10px;">
										<span style="font-size: 13px;">已完成告警</span>
									</el-row>
									<el-row style="padding-bottom: 10px;">
										<span style="font-size: 24px;color: #00deff;text-shadow: 0 0 5px #00deff;font-family: electronicFont;">16</span>
										<i class="text-d" style="font-size: 12px;color: #ff6316;">↑4.5%</i>
									</el-row>
								</div>
							</div>
						</div>
					</el-col>
				</el-row>
				
				
				
				
				<el-row style="padding-top: 400px;">
					<div></div>
				</el-row>
				
				<el-row style="background-color: rgba(22, 31, 38, 0.7);">
					<el-row>
						<div class="titlebox" >
							<span style="font-size: 20px;font-weight:500;color:white;padding-left: 20px;text-shadow: 0.3rem 0 0.3rem #c1faff;">人员管控</span>
						</div>
					</el-row>
					<el-row>
						<el-col :span="8">
							<el-row style="padding-top: 10px;">
								<span style="color: white;font-size: 15px;font-weight: 500;padding-left: 10px;">
									外来访客
								</span>
							</el-row>
							<el-row>
								<el-col :span="12">
									<div style="padding-left: 5px;padding-top: 10px;">
										<div class="kuang" style="color: white;height: 35px;width: 150px;">
											<div style="padding-left: 10px; ">
												<el-col :span="5">
													<span style="font-size: 1px;zoom:0.8">本周访客人数</span>
												</el-col>
												<el-col :span="19">
													<span style="font-size: 24px;color: #00deff;text-shadow: 0 0 5px #00deff;font-family: electronicFont;padding-left: 20px;">32</span>
													<!-- <i class="text-d" style="font-size: 12px;color: #ff6316;">↑4.01%</i> -->
												</el-col>
												
											</div>
										</div>
									</div>
								</el-col>
								<el-col :span="12">
									<div style="padding-left: 5px;padding-top: 10px;">
										<div class="kuang" style="color: white;height: 35px;width: 150px;">
											<div style="padding-left: 10px; ">
												<el-col :span="5">
													<span style="font-size: 1px;zoom:0.8">拒绝访客数</span>
												</el-col>
												<el-col :span="19">
													<span style="font-size: 24px;color: #00deff;text-shadow: 0 0 5px #00deff;font-family: electronicFont;padding-left: 20px;">7</span>
													<!-- <i class="text-d" style="font-size: 12px;color: #ff6316;">↑4.01%</i> -->
												</el-col>
												
											</div>
										</div>
									</div>
								</el-col>
							</el-row>
							<el-row>
								<div id="char9" style="height: 150px;width:220px;"></div>
							</el-row>
						</el-col>
						<el-col :span="8">
							<el-row style="padding-top: 10px;">
								<span style="color: white;font-size: 15px;font-weight: 500;padding-left: 10px;">
									归寝概况
								</span>
							</el-row>
							<el-row>
								<el-col :span="12">
									<div style="padding-left: 5px;padding-top: 10px;">
										<div class="kuang" style="color: white;height: 35px;width: 150px;">
											<div style="padding-left: 10px; ">
												<el-col :span="5">
													<span style="font-size: 1px;zoom:0.8">本周归寝人数</span>
												</el-col>
												<el-col :span="19">
													<span style="font-size: 24px;color: #00deff;text-shadow: 0 0 5px #00deff;font-family: electronicFont;padding-left: 20px;">1020</span>
													<!-- <i class="text-d" style="font-size: 12px;color: #ff6316;">↑4.01%</i> -->
												</el-col>
												
											</div>
										</div>
									</div>
								</el-col>
								<el-col :span="12">
									<div style="padding-left: 5px;padding-top: 10px;">
										<div class="kuang" style="color: white;height: 35px;width: 150px;">
											<div style="padding-left: 10px; ">
												<el-col :span="5">
													<span style="font-size: 1px;zoom:0.8">异常归寝人数</span>
												</el-col>
												<el-col :span="19">
													<span style="font-size: 24px;color: #00deff;text-shadow: 0 0 5px #00deff;font-family: electronicFont;padding-left: 20px;">30</span>
													<!-- <i class="text-d" style="font-size: 12px;color: #ff6316;">↑4.01%</i> -->
												</el-col>
												
											</div>
										</div>
									</div>
								</el-col>
							</el-row>
							<el-row>
								<div id="char8" style="height: 150px;width:220px;"></div>
							</el-row>
						</el-col>
						
						<el-col :span="8">
							<el-row style="padding-top: 10px;">
								<span style="color: white;font-size: 15px;font-weight: 500;padding-left: 10px;">
									值班到岗
								</span>
							</el-row>
							<el-row>
								<el-col :span="12">
									<div style="padding-left: 5px;padding-top: 10px;">
										<div class="kuang" style="color: white;height: 35px;width: 150px;">
											<div style="padding-left: 10px; ">
												<el-col :span="5">
													<span style="font-size: 1px;zoom:0.8">本周到岗人数</span>
												</el-col>
												<el-col :span="19">
													<span style="font-size: 24px;color: #00deff;text-shadow: 0 0 5px #00deff;font-family: electronicFont;padding-left: 20px;">54</span>
													<!-- <i class="text-d" style="font-size: 12px;color: #ff6316;">↑4.01%</i> -->
												</el-col>
												
											</div>
										</div>
									</div>
								</el-col>
								<el-col :span="12">
									<div style="padding-left: 5px;padding-top: 10px;">
										<div class="kuang" style="color: white;height: 35px;width: 150px;">
											<div style="padding-left: 10px; ">
												<el-col :span="5">
													<span style="font-size: 1px;zoom:0.8">异常到岗人数</span>
												</el-col>
												<el-col :span="19">
													<span style="font-size: 24px;color: #00deff;text-shadow: 0 0 5px #00deff;font-family: electronicFont;padding-left: 20px;">8</span>
													<!-- <i class="text-d" style="font-size: 12px;color: #ff6316;">↑4.01%</i> -->
												</el-col>
												
											</div>
										</div>
									</div>
								</el-col>
							</el-row>
							<el-row>
								<div id="char10" style="height: 150px;width:220px;"></div>
							</el-row>
						</el-col>
						
					</el-row>
				</el-row>
				
			</el-col>
			
			
			
			
			<el-col  :span="6" style="padding-left: 20px;padding-top: 30px;float:right;padding-right: 20px;">
				<el-row style="background-color: rgba(22, 31, 38, 0.7);">
					<el-row>
						<div class="titlebox" >
							<span style="font-size: 20px;font-weight:500;color:white;padding-left: 20px;text-shadow: 0.3rem 0 0.3rem #c1faff;">设备运维</span>
						</div>
					</el-row>
					<el-row>
						<div style="display: flex;padding-top: 15px;">
							<span style="color: white;font-size: 15px;font-weight: 500;padding-left: 10px;">监控状态</span>
						</div>
					</el-row>
					<el-row style="padding-top: 15px;">
						<div class="Echarts">
						  <div id="char2" style="width:`180px;height: 80px;"></div>
						</div>
					</el-row>
					<el-row>
						<div style="display: flex;">
							<span style="color: white;font-size: 15px;font-weight: 500;padding-left: 10px;">监控分布</span>
						</div>
					</el-row>
					<el-row>
						<div style="padding-top: 5px;">
							<div id="char3" style="width:`180px;height: 100px;"></div>
						</div>
					</el-row>
				</el-row>
				
				<el-row style="padding-top: 20px;">
					<div></div>
				</el-row>
				
				
				<el-row style="background-color: rgba(22, 31, 38, 0.7);">
					<el-row>
						<div class="titlebox" >
							<span style="font-size: 20px;font-weight:500;color:white;padding-left: 20px;text-shadow: 0.3rem 0 0.3rem #c1faff;">交通态势</span>
						</div>
					</el-row>
					<el-row>
						<div style="display: flex;padding-top: 15px;">
							<span style="color: white;font-size: 15px;font-weight: 500;padding-left: 10px;">交通警情</span>
						</div>
					</el-row>
					<el-row style="">
						<div style="padding-left: 50px;padding-right: 20px;zoom:0.8">
						  <div id="char5" style="width:`220px;height: 200px;"></div>
						</div>
					</el-row>
					<el-row>
						<div style="display: flex;">
							<span style="color: white;font-size: 15px;font-weight: 500;padding-left: 10px;">交通流量</span>
						</div>
					</el-row>
					<el-row style="padding-top: 15px;">
						<div class="Echarts" style="padding-left: 10px;padding-right: 20px;">
						  <div id="char4" style="width:`180px;height: 170px;"></div>
						</div>
					</el-row>
				</el-row>
			</el-col>
		</el-row>
		
		
		
		
    	
		
    	
    </div>
    

  </div>
</template>



<script>
import PanelGroup from './dashboard/PanelGroup'
import LineChart from './dashboard/LineChart'
import RaddarChart from './dashboard/RaddarChart'
import PieChart from './dashboard/PieChart'
import BarChart from './dashboard/BarChart'
// import {Navbar} from '../layout/components/Navbar.vue'
const lineChartData = {
  newVisitis: {
    expectedData: [100, 120, 161, 134, 105, 160, 165],
    actualData: [120, 82, 91, 154, 162, 140, 145]
  },
  messages: {
    expectedData: [200, 192, 120, 144, 160, 130, 140],
    actualData: [180, 160, 151, 106, 145, 150, 130]
  },
  purchases: {
    expectedData: [80, 100, 121, 104, 105, 90, 100],
    actualData: [120, 90, 100, 138, 142, 130, 130]
  },
  shoppings: {
    expectedData: [130, 140, 141, 142, 145, 150, 160],
    actualData: [120, 82, 91, 154, 162, 140, 130]
  }
}
export default {
  name: "index",
  components: {
    PanelGroup,
    LineChart,
    RaddarChart,
    PieChart,
    BarChart
  },
  data() {
    return {
      newTime: "",
	  lineChartData: lineChartData.newVisitis

    };
  },
  mounted(){
          this.getNowTime();//进入页面调用该方法获取当前时间
          clearInterval(myTimeDisplay );//销毁之前定时器
          var myTimeDisplay = setInterval(() => {
             this.getNowTime(); //每秒更新一次时间
          }, 1000);    
		  this.myEcharts();
		  this.myEcharts1();
		  this.myEcharts4();
		  this.myEcharts5();
		  this.myEcharts6();
		  this.myEcharts7();
		  this.myEcharts8();
		  this.myEcharts9();
		  this.myEcharts10();
  },
  methods: {
	  handleSetLineChartData(type) {
	    this.lineChartData = lineChartData[type]
	  },
		getNowTime() {
		            var date = new Date();
		            var time = date.getFullYear() + '-' + (date.getMonth() + 1) + '-' + date.getDate() + ' ' + date.getHours() + ':' + date.getMinutes() + ':' + date.getSeconds();
		            this.newTime = time;
		        },
		       //根据自己的需求，看要不要在时间不大于10的时候在前面补0，如果需要直接this.addZero(date.getMinutes()),其它与之相同，如果不需要删掉addZero（）方法即可。
		       //小于10的拼接上0字符串
		        addZero(s) {
		            return s < 10 ? ('0' + s) : s;
		        },
		myEcharts(){
				  // 基于准备好的dom，初始化echarts实例
				  var myChart = this.$echarts.init(document.getElementById('char2'));
				  // 指定图表的配置项和数据
				  var option = {
					  tooltip : {
					      trigger: 'axis',
					      axisPointer : {            // 坐标轴指示器，坐标轴触发有效
					          type : 'shadow'        // 默认为直线，可选为：'line' | 'shadow'
					      }
					  },
					  grid: {show:'true',borderWidth:'0'},
					  legend: {
					      data:['在线', '离线','故障','维修'],
					      textStyle : {
					          color : '#ffffff',
					  		fontSize:10
					      }
					  },
					  color:['rgba(58,224,52,0.5)','rgba(199,134,153,0.5)','rgba(27,159,255,0.5)','rgba(213,116,7,0.5)'],
					  calculable :false,
					  xAxis : [
					      {
					          type : 'value',
					          axisLabel: {
					              show: true,
					              textStyle: {
					                  color: '#fff'
					              }
					          },
					          splitLine:{
					              lineStyle:{
					                  color:['#f2f2f2'],
					                  width:0,
					                  type:'solid'
					              }
					          },
					  		axisTick:{
					  			  show:false//不显示坐标轴刻度线
					  		},
					  		axisLine: {
					  			  show: false,//不显示坐标轴线
					  		},
					  		axisLabel: {
					  			  show: false,//不显示坐标轴上的文字
					  		}
					      }
					  ],
					  yAxis : [
					      {
					          type : 'category',
					          data : ['设备'],
					          axisLabel: {
					              show: false,
					              textStyle: {
					                  color: '#fff'
					              }
					          },
					          splitLine:{
					              lineStyle:{
					                  width:0,
					                  type:'solid'
					              },
					  			show:false
					          },
					  		axisTick:{
					  		    show: false
					  		},
					  		axisLine: { //轴线
					  		          show: false
					  		        },
					      },
					  
					  ],
					  series : [
					      {
					          name:'在线',
					          type:'bar',
					          stack: '总量',
					          itemStyle : { normal: {label : {show: true, position: 'insideRight'},borderWidth: 1,
					  		borderColor: '#3ae034'},
					  		},
					  		            
					          data:[60],
					  		barWidth : 20,
					      },
					      {
					          name:'离线',
					          type:'bar',
					          stack: '总量',
					          itemStyle : { normal: {label : {show: true, position: 'insideRight'},borderWidth: 1,borderColor:'#778699'}},
					          data:[5],
					  		barWidth : 20,
					      },
					      {
					          name:'故障',
					          type:'bar',
					          stack: '总量',
					          itemStyle : { normal: {label : {show: true, position: 'insideRight'},borderWidth: 1,borderColor:'#1b9fff'}},
					          data:[2],
					  		barWidth : 20,
					      },
					      {
					          name:'维修',
					          type:'bar',
					          stack: '总量',
					          itemStyle : { normal: {label : {show: true, position: 'insideRight'},borderWidth: 1,borderColor:'#e77407'}},
					          data:[3],
					  		barWidth : 20,
					      }
					  
					  ]
				  };
		
				  // 使用刚指定的配置项和数据显示图表。
				  myChart.setOption(option);
	},
	myEcharts1(){
		  // 基于准备好的dom，初始化echarts实例
		  var myChart1 = this.$echarts.init(document.getElementById('char3'));
		  var option1 = {
		    //  backgroundColor: '#00265f',
		      tooltip: {
		          trigger: 'axis',
		          axisPointer: { type: 'shadow'}
		      },
		      grid: {
		          left: '2%',
		  		top:'10px',
		          right: '3%',
		          bottom: '12%',
		         containLabel: true
		      },
		      xAxis: [{
		          type: 'category',
		  		data:['东门','西门','南门','北门','教学区','寝室区','行政楼','体育馆','艺术楼','食堂'],
		          axisLine: {
		              show: true,
		           lineStyle: {
		                  color: "rgba(255,255,255,.1)",
		                  width: 1,
		                  type: "solid"
		              },
		          },
		  		
		          axisTick: {
		              show: false,
		          },
		  		axisLabel:  {
		                  interval: 0,
		                  rotate:0,
		                  show: true,
		                  splitNumber: 15,
		                  textStyle: {
		   					color: "white",
		                      fontSize: '8',
		                  },
		              },
		      }],
		      yAxis: [{
		          type: 'value',
		          axisLabel: {
		             //formatter: '{value} %'
		  			show:true,
		  			 textStyle: {
		   					color: "white",
		                      fontSize: '10',
		                  },
		          },
		          axisTick: {
		              show: false,
		          },
		          axisLine: {
		              show: true,
		              lineStyle: {
		                  color: "rgba(255,255,255,.1	)",
		                  width: 1,
		                  type: "solid"
		              },
		          },
		          splitLine: {
		              lineStyle: {
		                 color: "rgba(255,255,255,.1)",
		              }
		          }
		      }],
		      series: [
		  		{
		          type: 'bar',
		          data: [10,20,30,30,20,45,20,38,29,30],
		          barWidth:'35%', //柱子宽度
		         barGap: 8, //柱子之间间距
		          itemStyle: {
		              normal: {
		                  color:'#27d08a',
		                  opacity: 1,
		  				barBorderRadius: 5,
		              }
		          }
		      }
		  		
		  	]
		  };
		  myChart1.setOption(option1);
	},
	myEcharts4(){
				  // 基于准备好的dom，初始化echarts实例
				  var myChart4 = this.$echarts.init(document.getElementById('char4'));
				  
				  
				  //车流量
				  var data = {
				      id: 'multipleBarsLines',
				      legendBar: ['人流量', '车流量'],
				      symbol: ' ', //数值是否带百分号        --默认为空 ''
				      // legendLine: ['环比', '同比'],
				      xAxis: ['0时','4时','8时','12时','16时','20时','23时'],
				      yAxis: [
				          [8, 10, 10, 11, 4, 13,8],
				          [10, 7, 8, 8, 7, 9,7]
				      ],
				      // lines: [
				      //     [10, 10, 9, 11, 7, 4,5],
				      //     [6, 12, 12, 2, 4, 4,2]
				      // ],
				      barColor: ['#00e3c1', '#13c9ff'], //柱子颜色 必填参数
				      // lineColor: ['#fd6665', '#fba73b'], // 折线颜色
				  }
				  
				  var myData = (function test() {
				      let yAxis = data.yAxis || []
				      let lines = data.lines || []
				      let legendBar = data.legendBar || []
				      let legendLine = data.legendLine || []
				      var symbol = data.symbol || ' '
				      let seriesArr = []
				      let legendArr = []
				      yAxis && yAxis.forEach((item, index) => {
				          legendArr.push({
				              name: legendBar && legendBar.length > 0 && legendBar[index]
				          })
				          seriesArr.push({
				              name: legendBar && legendBar.length > 0 && legendBar[index],
				              type: 'bar',
				              barGap: '0.5px',
				              data: item,
				              barWidth: data.barWidth || 8,
				              label: {
				                  normal: {
				                      show: false,
				                      formatter: '{c}' + symbol,
				                      position: 'top',
				                      textStyle: {
				                          color: '#000',
				                          fontStyle: 'normal',
				                          fontFamily: '微软雅黑',
				                          textAlign: 'left',
				                          fontSize: 11,
				                      },
				                  },
				              },
				              itemStyle: { //图形样式
				                  normal: {
				                      barBorderRadius:0,
				                      borderWidth:1,
				                      borderColor:'#ddd',
				                      color: data.barColor[index]
				                  },
				              }
				          })
				      })
				  
				      lines && lines.forEach((item, index) => {
				          legendArr.push({
				              name: legendLine && legendLine.length > 0 && legendLine[index]
				          })
				          seriesArr.push({
				              name: legendLine && legendLine.length > 0 && legendLine[index],
				              type: 'line',
				              data: item,
				              itemStyle: {
				                  normal: {
				                      color: data.lineColor[index],
				                      lineStyle: {
				                          width: 2,//折线宽度
				                          type: 'solid',
				                      }
				                  }
				              },
				              label: {
				                  normal: {
				                      show: false, //折线上方label控制显示隐藏
				                      position: 'top',
				                  }
				              },
				              symbol: 'circle',
				              symbolSize: 5
				          })
				      })
				  
				      return {
				          seriesArr,
				          legendArr
				      }
				  })()
				  
				  
				  
				  
				  // 指定图表的配置项和数据
				  var option4= {
				      title: {
				          show: true,
				          text: data.title,
				          subtext: data.subTitle,
				          link: '1111'
				      },
				      tooltip: {
				          trigger: 'axis',
				          formatter: function(params) {
				              var time = '';
				              var str = '';
				              for (var i of params) {
				                  time = i.name.replace(/\n/g, '') + '<br/>';
				                  if (i.data == 'null' || i.data == null) {
				                      str += i.seriesName + '：无数据' + '<br/>'
				                  } else {
				                      str += i.seriesName + '：' + i.data + symbol + '%<br/>'
				                  }
				  
				              }
				              return time + str;
				          },
				          axisPointer: {
				              type: 'none'
				          },
				      },
				      legend: {
				          right: data.legendRight || '30%',
				          top: 0,
				          right:10,
				          itemGap: 16,
				          itemWidth: 10,
				          itemHeight: 10,
				          data: myData.legendArr,
				          textStyle: {
				              color: '#fff',
				              fontStyle: 'normal',
				              fontFamily: '微软雅黑',
				              fontSize: 12,
				          }
				      },
				      grid: {
				          x: 0,
				          y: 30,
				          x2: 0,
				          y2: 25,
				      },
				      xAxis: {
				          type: 'category',
				          data: data.xAxis,
				          axisTick: {
				              show: false,
				          },
				  
				          axisLine: {
				              show: false,
				          },
				          axisLabel: {       //轴标
				              show: true,
				              interval: 0,
				              textStyle: {
				                  lineHeight:5,
				                  padding: [2, 2, 0, 2],
				                  height: 50,
				                  fontSize: 12,
				                  color:'#fff',
				              },
				              rich: {
				                  Sunny: {
				                      height: 50,
				                      // width: 60,
				                      padding: [0, 5, 0, 5],
				                      align: 'center',
				                  },
				              },
				              formatter: function(params, index) {
				                  var newParamsName = "";
				                  var splitNumber = 5;
				                  var paramsNameNumber = params && params.length;
				                  if (paramsNameNumber && paramsNameNumber <= 4) {
				                      splitNumber = 4;
				                  } else if (paramsNameNumber >= 5 && paramsNameNumber <= 7) {
				                      splitNumber = 4;
				                  } else if (paramsNameNumber >= 8 && paramsNameNumber <= 9) {
				                      splitNumber = 5;
				                  } else if (paramsNameNumber >= 10 && paramsNameNumber <= 14) {
				                      splitNumber = 5;
				                  } else {
				                      params = params && params.slice(0, 15);
				                  }
				  
				                  var provideNumber = splitNumber; //一行显示几个字
				                  var rowNumber = Math.ceil(paramsNameNumber / provideNumber) || 0;
				                  if (paramsNameNumber > provideNumber) {
				                      for (var p = 0; p < rowNumber; p++) {
				                          var tempStr = "";
				                          var start = p * provideNumber;
				                          var end = start + provideNumber;
				                          if (p == rowNumber - 1) {
				                              tempStr = params.substring(start, paramsNameNumber);
				                          } else {
				                              tempStr = params.substring(start, end) + "\n";
				                          }
				                          newParamsName += tempStr;
				                      }
				  
				                  } else {
				                      newParamsName = params;
				                  }
				                  params = newParamsName
				                  return '{Sunny|' + params + '}';
				              },
				              color: '#687284',
				          },
				  
				      },
				      yAxis: {
				          axisLine: {
				              show: false
				          },
				          axisTick: {
				              show: false
				          },
				          axisLabel: {
				              show: false
				          },
				          splitLine: {
				              show: true,
				              lineStyle: {
				                  color: '#F1F3F5',
				                  type: 'solid'
				              },
				              interval: 2
				          },
				          splitNumber: 4,
				      },
				      series: myData.seriesArr
				  };
		
				  // 使用刚指定的配置项和数据显示图表。
				  myChart4.setOption(option4);
	},
	myEcharts5(){
				  // 基于准备好的dom，初始化echarts实例
				  var myChart5 = this.$echarts.init(document.getElementById('char5'));
				  
				  //违法原因
				  var dataArr = [
				      {name: '闯红灯', value: 300},
				      {name: '车辆违停', value: 500},
				      {name: '闯禁行', value: 400},
				      {name: '未戴头盔', value: 350},
				  ]
				  var data = dataArr
				  var option5 = {
				      color: ['#F77474', '#47F6A2', '#FF5937', '#F3DB5D'],
				  	// '#FF5937','#F3DB5D','#F77474','#28DCCF',
				      tooltip : {
				          trigger: 'item',
				          formatter: "{a} <br/>{b} : {c} ({d}%)"
				      },
				      series: [
				          {
				              name: '路况类型占比',
				              type: 'pie',
				              radius: ['50%', '70%'],
				              center: ['53%', '55%'],
				              labelLine: {
				                  normal: {
				                      length: 12,
				                      lineStyle: {
				                          type: 'solid',
				                          color: '#0EFCFF'
				                      }
				                  }
				  			
				              },
				              label: {
				                  normal: {
				                      formatter: (params)=>{
				                          return params.name
				                      },
				                      borderWidth: 0,
				                      borderRadius: 4,
				                      padding: [0,0],
				                      height: 20,
				                      fontSize: 10,
				                      align: 'center',
				                      color: '#0EFCFF',
				                  }
				              },
				              data: data
				          },
				          {
				              color: '#0EFCFF',
				              type: 'pie',
				              radius: ['87', '88'],
				              center: ['53%', '55%'],
				              data: [100],
				              label: {
				                  show: false
				              }
				          },
				          {
				              type: 'pie',
				              radius: ['45', '46'],
				              center: ['53%', '55%'],
				              data: [100],
				              label: {
				                  show: false
				              }
				          }
				      ]
				  };
				  // 使用刚指定的配置项和数据显示图表。
				  myChart5.setOption(option5);
	},
	
	myEcharts6(){
				  // 基于准备好的dom，初始化echarts实例
				  var myChart6 = this.$echarts.init(document.getElementById('char6'));
				  
				  // 指定图表的配置项和数据
				  var option6 = {
				  
				      tooltip : {
				          trigger: 'item',
				          formatter: "{b}: <br/>  {c} ({d}%)"
				      },
				  
				      toolbox: {
				          show : false,
				          feature : {
				              mark : {show: true},
				              dataView : {show: true, readOnly: false},
				              magicType : {
				                  show: true,
				                  type: ['pie', 'funnel']
				              },
				              restore : {show: true},
				              saveAsImage : {show: true}
				          }
				      },
				      calculable : true,
				      series : [
				  
				          {
				              name:'车辆类型',
				              type:'pie',
				              color: ['#d0a3ff', '#29cd81', '#ff999a', '#02afff','#25f3e6','#f5c847'],
				              radius : [10, 70],
				              center : ['50%', '50%'],
				              roseType : 'area',
				              data:[
				                  {value:180, name:'消防栓'},
				                  {value:150, name:'消防通道'},
				                  {value:100, name:'灭火器'},
				                  {value:300, name:'消控室'},
				                  {value:420, name:'微型消防站'},
				  				{value:500, name:'其他'}
				              ],
				  			labelLine:{  
				  				normal:{  
				  					length:3
				  				}  
				  			}, 
				          }
				      ]
				  };
				  // 使用刚指定的配置项和数据显示图表。
				  myChart6.setOption(option6);
	},
	myEcharts7(){
				  // 基于准备好的dom，初始化echarts实例
				  var myChart7 = this.$echarts.init(document.getElementById('char7'));
		
				  // 指定图表的配置项和数据
				  var option7 = {
	  title: {},
	  tooltip: {
	    trigger: 'axis',
	    axisPointer: {
	      type: 'shadow'
	    }
	  },
	  legend: {},
	  grid: {
		  top:"10%",
	    left: '3%',
	    right: '10%',
	    bottom: '10%',
	    containLabel: true
	  },
	  xAxis: {
	    type: 'value',
	    boundaryGap: [0, 0.3],
		splitLine:{show: false},
		max:100,
		axisLabel:  {
		          // interval: 0,
		          // rotate:0,
		          show: true,
		          // splitNumber: 15,
		          textStyle: {
					color: "white",
		              fontSize: '8',
		          },
		      },
	  },
	  yAxis: {
	    type: 'category',
	    data: ['食堂六', '食堂五', '食堂四', '食堂三', '食堂二', '食堂一'],
		splitLine:{show: false},
		axisLabel:  {
		          // interval: 0,
		          // rotate:0,
		          show: true,
		          // splitNumber: 15,
		          textStyle: {
					color: "white",
		              fontSize: '8',
		          },
		      },
	  },
	  series: [
	    {
	      type: 'bar',
	      data: [60, 74, 85, 89, 90, 95],
		   barGap:'80%',/*多个并排柱子设置柱子之间的间距*/
		  barCategoryGap:'50%',/*多个并排柱子设置柱子之间的间距*/
		  itemStyle:{
			  normal:{
				  color:'#69c5b7',
				  
			  }
		  },
		  barWidth: '30%',
	    }
	  ]
	};
				  // 使用刚指定的配置项和数据显示图表。
		  myChart7.setOption(option7);
	},
	myEcharts8(){
		  // 基于准备好的dom，初始化echarts实例
		  var myChart8 = this.$echarts.init(document.getElementById('char8'));
		  var option8 = {
		    //  backgroundColor: '#00265f',
		      tooltip: {
		          trigger: 'axis',
		          axisPointer: { type: 'shadow'}
		      },
		      grid: {
		          left: '2%',
		  		top:'20px',
		          right: '3%',
		          bottom: '20%',
		         containLabel: true
		      },
		      xAxis: [{
		          type: 'category',
		  		data:['周一','周二','周三','周四','周五','周六','周日'],
		          axisLine: {
		              show: true,
		           lineStyle: {
		                  color: "rgba(255,255,255,.1)",
		                  width: 1,
		                  type: "solid"
		              },
		          },
		  		
		          axisTick: {
		              show: false,
		          },
		  		axisLabel:  {
		                  interval: 0,
		                  rotate:0,
		                  show: true,
		                  splitNumber: 15,
		                  textStyle: {
		   					color: "white",
		                      fontSize: '8',
		                  },
		              },
		      }],
		      yAxis: [{
		          type: 'value',
		          axisLabel: {
		             //formatter: '{value} %'
		  			show:true,
		  			 textStyle: {
		   					color: "white",
		                      fontSize: '10',
		                  },
		          },
		          axisTick: {
		              show: false,
		          },
		          axisLine: {
		              show: true,
		              lineStyle: {
		                  color: "rgba(255,255,255,.1	)",
		                  width: 1,
		                  type: "solid"
		              },
		          },
		          splitLine: {
		              lineStyle: {
		                 color: "rgba(255,255,255,.1)",
		              }
		          }
		      }],
		      series: [
		  		{
		          type: 'line',
		          data: [1500, 1200, 600, 200, 300, 300, 900,1500, 1200, 600,300, 300, 900,1500, 1200, 600],
		          barWidth:'35%', //柱子宽度
		         barGap: 8, //柱子之间间距
		          itemStyle: {
		              normal: {
		                  color:'rgba(64, 230, 255, 0.8)',
		                  opacity: 1,
		  				barBorderRadius: 5,
		              }
		          },
				  areaStyle: {            // 折现下是否填充
				  			color: {
				  				type: 'linear',
				  				x: 0,
				  				y: 0,
				  				x2: 0,
				  				y2: 1,
				  				colorStops: [{
				  					offset: 0, color: 'rgba(64, 230, 255, 0.5)' // 0% 处的颜色
				  				}, {
				  					offset: 1, color: 'rgba(0,0,0,0.1)' // 100% 处的颜色
				  				}],
				  				global: false
				  			}
				  		},
		      }
		  		
		  	]
		  };
		  myChart8.setOption(option8);
	},
	myEcharts9(){
		  // 基于准备好的dom，初始化echarts实例
		  var myChart9 = this.$echarts.init(document.getElementById('char9'));
		  var option9 = {
		    //  backgroundColor: '#00265f',
		      tooltip: {
		          trigger: 'axis',
		          axisPointer: { type: 'shadow'}
		      },
		      grid: {
		          left: '2%',
		  		top:'20px',
		          right: '3%',
		          bottom: '20%',
		         containLabel: true
		      },
		      xAxis: [{
		          type: 'category',
		  		data:['周一','周二','周三','周四','周五','周六','周日'],
		          axisLine: {
		              show: true,
		           lineStyle: {
		                  color: "rgba(255,255,255,.1)",
		                  width: 1,
		                  type: "solid"
		              },
		          },
		  		
		          axisTick: {
		              show: false,
		          },
		  		axisLabel:  {
		                  interval: 0,
		                  rotate:0,
		                  show: true,
		                  splitNumber: 15,
		                  textStyle: {
		   					color: "white",
		                      fontSize: '8',
		                  },
		              },
		      }],
		      yAxis: [{
		          type: 'value',
		          axisLabel: {
		             //formatter: '{value} %'
		  			show:true,
		  			 textStyle: {
		   					color: "white",
		                      fontSize: '10',
		                  },
		          },
		          axisTick: {
		              show: false,
		          },
		          axisLine: {
		              show: true,
		              lineStyle: {
		                  color: "rgba(255,255,255,.1	)",
		                  width: 1,
		                  type: "solid"
		              },
		          },
		          splitLine: {
		              lineStyle: {
		                 color: "rgba(255,255,255,.1)",
		              }
		          }
		      }],
		      series: [
		  		{
		          type: 'line',
		          data: [1500, 1200, 600, 200, 300, 300, 900,1500, 1200, 600,300, 300, 900,1500, 1200, 600],
		          barWidth:'35%', //柱子宽度
		         barGap: 8, //柱子之间间距
		          itemStyle: {
		              normal: {
		                  color:'rgba(64, 230, 255, 0.8)',
		                  opacity: 1,
		  				barBorderRadius: 5,
		              }
		          },
				  areaStyle: {            // 折现下是否填充
				  			color: {
				  				type: 'linear',
				  				x: 0,
				  				y: 0,
				  				x2: 0,
				  				y2: 1,
				  				colorStops: [{
				  					offset: 0, color: 'rgba(64, 230, 255, 0.5)' // 0% 处的颜色
				  				}, {
				  					offset: 1, color: 'rgba(0,0,0,0.1)' // 100% 处的颜色
				  				}],
				  				global: false
				  			}
				  		},
		      }
		  		
		  	]
		  };
		  myChart9.setOption(option9);
	},
	myEcharts10(){
		  // 基于准备好的dom，初始化echarts实例
		  var myChart10 = this.$echarts.init(document.getElementById('char10'));
		  var option10 = {
		    //  backgroundColor: '#00265f',
		      tooltip: {
		          trigger: 'axis',
		          axisPointer: { type: 'shadow'}
		      },
		      grid: {
		          left: '2%',
		  		top:'20px',
		          right: '3%',
		          bottom: '20%',
		         containLabel: true
		      },
		      xAxis: [{
		          type: 'category',
		  		data:['周一','周二','周三','周四','周五','周六','周日'],
		          axisLine: {
		              show: true,
		           lineStyle: {
		                  color: "rgba(255,255,255,.1)",
		                  width: 1,
		                  type: "solid"
		              },
		          },
		  		
		          axisTick: {
		              show: false,
		          },
		  		axisLabel:  {
		                  interval: 0,
		                  rotate:0,
		                  show: true,
		                  splitNumber: 15,
		                  textStyle: {
		   					color: "white",
		                      fontSize: '8',
		                  },
		              },
		      }],
		      yAxis: [{
		          type: 'value',
		          axisLabel: {
		             //formatter: '{value} %'
		  			show:true,
		  			 textStyle: {
		   					color: "white",
		                      fontSize: '10',
		                  },
		          },
		          axisTick: {
		              show: false,
		          },
		          axisLine: {
		              show: true,
		              lineStyle: {
		                  color: "rgba(255,255,255,.1	)",
		                  width: 1,
		                  type: "solid"
		              },
		          },
		          splitLine: {
		              lineStyle: {
		                 color: "rgba(255,255,255,.1)",
		              }
		          }
		      }],
		      series: [
		  		{
		          type: 'line',
		          data: [1500, 1200, 600, 200, 300, 300, 900,1500, 1200, 600,300, 300, 900,1500, 1200, 600],
		          barWidth:'35%', //柱子宽度
		         barGap: 8, //柱子之间间距
		          itemStyle: {
		              normal: {
		                  color:'rgba(64, 230, 255, 0.8)',
		                  opacity: 1,
		  				barBorderRadius: 5,
		              }
		          },
				  areaStyle: {            // 折现下是否填充
				  			color: {
				  				type: 'linear',
				  				x: 0,
				  				y: 0,
				  				x2: 0,
				  				y2: 1,
				  				colorStops: [{
				  					offset: 0, color: 'rgba(64, 230, 255, 0.5)' // 0% 处的颜色
				  				}, {
				  					offset: 1, color: 'rgba(0,0,0,0.1)' // 100% 处的颜色
				  				}],
				  				global: false
				  			}
				  		},
		      }
		  		
		  	]
		  };
		  myChart10.setOption(option10);
	},
	
	
	
	
	
	
	



	
	
	
	
	
	
	
	
	
  },
};
</script>

<style scoped lang="scss">
	
.kuang{
	background: url(../assets/images/kuang.png) no-repeat;
	background-size: 65% 100%;
}
.kuang0{
	background: url(../assets/images/kuang0.png) no-repeat;
	background-size: 65% 100%;
}
.kuang5{
	background: url(../assets/images/kuang5.png) no-repeat;
	background-size: 65% 100%;
}

.titlebox{
	// width: 4.9rem;
	// height: 0.42rem;
	background: url(../assets/images/title.png) top left no-repeat;
	background-size: 100% 100%;
	margin: auto;
	display: flex;
	flex-flow: row nowrap;
	align-items: center;
	position: relative;
}   



	
	
.breathe-zct {
    position: relative;
    width: 20px;
    height: 20px;
    top: 2px;
    float: left;
    border: 1px solid #008000;
    border-radius: 20px;
    color: #fff;
    font-size: 10px;
    cursor: pointer;
    box-shadow: 0 1px 2px rgb(0 0 0 / 30%);
    overflow: hidden;
    background-image: -webkit-gradient(linear, left top, left bottom, from(#00FF00), to(#00FF00));
}
.breathe-zcts {
    position: relative;
    width: 40px;
    height: 40px;
    top: 2px;
    float: left;
    border: 1px solid #008000;
    border-radius: 20px;
    color: #fff;
    font-size: 20px;
    cursor: pointer;
    box-shadow: 0 1px 2px rgb(0 0 0 / 30%);
    overflow: hidden;
    background-image: -webkit-gradient(linear, left top, left bottom, from(#00FF00), to(#00FF00));
}
.breathe-yct {
    position: relative;
    width: 20px;
    height: 20px;
    top: 2px;
    float: left;
    border: 1px solid #008000;
    border-radius: 20px;
    color: #fff;
    font-size: 20px;
    cursor: pointer;
    box-shadow: 0 1px 2px rgb(0 0 0 / 30%);
    overflow: hidden;
    background-image: -webkit-gradient(linear, left top, left bottom, from(#FF0000), to(#FF0000));
}
.breathe-ycts {
    position: relative;
    width: 40px;
    height: 40px;
    top: 2px;
    float: left;
    border: 1px solid #008000;
    border-radius: 20px;
    color: #fff;
    font-size: 20px;
    cursor: pointer;
    box-shadow: 0 1px 2px rgb(0 0 0 / 30%);
    overflow: hidden;
    background-image: -webkit-gradient(linear, left top, left bottom, from(#FF0000), to(#FF0000));
}
.breathe-zc{ position:relative; width:25px; height:25px; margin:10px auto; line-height:40px; border:1px solid #008000; border-radius:20px; color:#fff; font-size:20px; text-align:center; cursor:pointer; box-shadow:0 1px 2px rgba(0,0,0,.3); overflow:hidden; 
			background-image: -webkit-gradient(linear, left top, left bottom, from(#00FF00), to(#00FF00));
			background-image: -moz-linear-gradient(#00FF00,#00FF00);
	    -webkit-animation-timing-function: ease-in-out;
	    -webkit-animation-name: breathe;
	    -webkit-animation-duration: 500ms;
	    -webkit-animation-iteration-count: infinite;
	    -webkit-animation-direction: alternate;
			animation:ease-in-out breathe 500ms infinite alternate; 
	}
	@keyframes breathe{
		0% { opacity: .2; box-shadow:0 1px 2px rgba(255,255,255,0.1);}
	    100% { opacity: 1; border:1px solid rgba(59,235,235,1); box-shadow:0 1px 30px rgba(59,255,255,1);}
	}
	@-webkit-keyframes breathe {
	    0% { opacity: .2; box-shadow:0 1px 2px rgba(255,255,255,0.1);}
	    100% { opacity: 1; border:1px solid rgba(59,235,235,1); box-shadow:0 1px 30px rgba(59,255,255,1);}
	}
	
	.breathe-yc{ position:relative; width:25px; height:25px; margin:10px auto; line-height:40px; border:1px solid #008000; border-radius:20px; color:#fff; font-size:20px; text-align:center; cursor:pointer; box-shadow:0 1px 2px rgba(0,0,0,.3); overflow:hidden; 
			background-image: -webkit-gradient(linear, left top, left bottom, from(#FF0000), to(#FF0000));
			background-image: -moz-linear-gradient(#FF0000,#FF0000);
	    -webkit-animation-timing-function: ease-in-out;
	    -webkit-animation-name: breathe;
	    -webkit-animation-duration: 1000ms;
	    -webkit-animation-iteration-count: infinite;
	    -webkit-animation-direction: alternate;
			animation:ease-in-out breathe 100ms infinite alternate; 
	}
	@keyframes breathe{
		0% { opacity: .2; box-shadow:0 1px 2px rgba(255,255,255,0.1);}
	    100% { opacity: 1; border:1px solid rgba(59,235,235,1); box-shadow:0 1px 30px rgba(59,255,255,1);}
	}
	@-webkit-keyframes breathe {
	    0% { opacity: .2; box-shadow:0 1px 2px rgba(255,255,255,0.1);}
	    100% { opacity: 1; border:1px solid rgba(59,235,235,1); box-shadow:0 1px 30px rgba(59,255,255,1);}
	}


.el-table, .el-table__expanded-cell {
	    background-color: transparent;
	}
	.el-table::before {
		 left: 0;
		 bottom: 0;
		 width: 100%;
		 height: 0px;
	}
	.el-table th, .el-table tr {
		color: white;
	    background-color: transparent;
	}
	.div-layout{
		height: 900px;
		background:url(../assets/images/school.png) no-repeat;
		background-size: 1370px 900px;
	}
	.div1{
		// background-image: url(../assets/images/kuang.png) no-repeat;
		background: url(../assets/images/kuang.png) no-repeat;
		background-size: 100% 100%;
		/* padding-top: 10px; */
		/* width: 520px;
		height: 300px; */
	}
	
	.visit{
		background: url(../assets/images/fangke1.png) no-repeat;
		background-size: 100% 100%;
	}
	
	
	


.home {
  blockquote {
    padding: 10px 20px;
    margin: 0 0 20px;
    font-size: 17.5px;
    border-left: 5px solid #eee;
  }
  hr {
    margin-top: 20px;
    margin-bottom: 20px;
    border: 0;
    border-top: 1px solid #eee;
  }
  .col-item {
    margin-bottom: 20px;
  }

  ul {
    padding: 0;
    margin: 0;
  }

  font-family: "open sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  color: #676a6c;
  overflow-x: hidden;

  ul {
    list-style-type: none;
  }

  h4 {
    margin-top: 0px;
  }

  h2 {
    margin-top: 10px;
    font-size: 26px;
    font-weight: 100;
  }

  p {
    margin-top: 10px;

    b {
      font-weight: 700;
    }
  }

  .update-log {
    ol {
      display: block;
      list-style-type: decimal;
      margin-block-start: 1em;
      margin-block-end: 1em;
      margin-inline-start: 0;
      margin-inline-end: 0;
      padding-inline-start: 40px;
    }
  }
}



</style>

