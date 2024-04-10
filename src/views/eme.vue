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
				<el-col :span="5">
					<el-row style="padding-top: 20px;padding-left: 20px;">
						<el-row style="background-color: rgba(22, 31, 38, 0.7);">
							<el-row>
								<div style="padding-left: 10px;">
									<div class="kuang6" style="height: 100px;width: 250px;">
										<div style="padding-top: 35px;padding-left: 75px;">
											<span style="font-size: 24px;color: white;">当前事件</span>
										</div>
									</div>
								</div>
							</el-row>
							<el-row style="color: white;">
								<div style="padding-top: 20px;">
									<div class="kuang" style="padding-left: 20px;padding-top: 20px;padding-bottom: 20px;">
										<el-row>
											<span>事件名称：&nbsp;&nbsp;烟雾明火</span>
										</el-row>
										<el-row>
											<span>告警类型：&nbsp;&nbsp;消防告警</span>
										</el-row>
										<el-row style="padding-top: 5px;">
											<span>事发时间：&nbsp;&nbsp;2023-04-15&nbsp;11:20:21</span>
										</el-row>
										<el-row style="padding-top: 5px;">
											<span>所属区域：&nbsp;&nbsp;校门口</span>
										</el-row>
										<el-row style="padding-top: 5px;">
											<span style="padding-left: 15px;">摄像头：&nbsp;&nbsp;校门口-东-1</span>
										</el-row>
									</div>
								</div>
							</el-row>
							<el-row style="color: white;">
								<div style="padding-top: 40px;">
									<div class="" style="padding-left: 30px;padding-top: 5px;padding-bottom: 20px;">
										<el-row>
											<!-- <span>一键报警：&nbsp;&nbsp;</span> -->
											<el-button style="background-color: #3ce7cb;color: ;" size="mini">一键报警110</el-button>
											<el-button style="background-color: #3ce7cb;color: ;" size="mini">一键报警120</el-button>
										</el-row>
										
									</div>
								</div>
							</el-row>
						</el-row>
					</el-row>
					
				</el-col>
				<el-col :span="7" >
					<span style="color: transparent;">22</span>
					
					
				</el-col>
				<el-col :span="12">
					<el-row style="padding-left: 20px;padding-top: 20px;">
						<div class="" style="background-color: rgba(22, 31, 38, 0.7);">
							<el-row>
								<div class="titlebox" >
									<span style="font-size: 20px;font-weight:550;color:white;padding-left: 540px;">校园监控</span>
								</div>
							</el-row>
							<el-row>
								<div class="kuang">
									<el-col :span="6">
										<el-row>
											<div class="kuang" style="height: 120px;">
												<template>
												    <div class='demo'>
												        <!-- <video-player class="video-player vjs-custom-skin" 
												                      ref="videoPlayer" 
												                      :playsinline="true" 
												                      :options="playerOptions">
												        </video-player> -->
												    </div>
												</template>
												
												<video autoplay="autoplay" controls width="98%" height="100%" style="padding-left: 2%;">
													<source src="videosrc" type="video/mp4"></source>
												</video>
												<!-- <vedio src="videosrc" poster="@/assets/images/firecar.png" controls autoplay="autoplay"></vedio> -->
												<!-- <video src="videosrc"  controls autoplay="autoplay"></video> -->
												<!-- <div class="item physical-video">
												    <div class="player">
												      
												    </div>
												  </div> -->
												<!-- <video autoplay="autoplay" width="98%" height="100%" style="padding-left: 2%;">
													<source src="videourl" type="video/mp4"></source>
												</video> -->
											</div>
										</el-row>
										<el-row>
											<div class="kuang" style="height: 110px;">
												<video src="videosrc" autoplay="autoplay" controls width="98%" height="100%" style="padding-left: 2%;">
													
												</video>
												<!-- <video ref="videosrc" controls controlslist="nodownload" autoplay
												     preload="none" width="600" height="300"    ：poster="img" ：src="videos">
												 </video> -->
												 <!-- <div class="player-container">
												
												            <video-player class="vjs-custom-skin" :options="playerOptions"></video-player>
												
												      </div> -->
												<!-- <video autoplay="autoplay" width="98%" height="100%" style="padding-left: 2%;">
													<source src="videourl" type="video/mp4"></source>
												</video> -->
											</div>
										</el-row>
										<el-row>
											<div class="kuang" style="height: 110px;">
												<video src="videosrc" autoplay="autoplay" controls width="98%" height="100%" style="padding-left: 2%;">
													
												</video>
												<!-- <video autoplay="autoplay" width="98%" height="100%" style="padding-left: 2%;">
													<source src="videourl" type="video/mp4"></source>
												</video> -->
											</div>
										</el-row>
									</el-col>
									<el-col :span="12">
										<el-row>
											<div class="kuang" style="height: 220px;">
												<video src="videosrc" autoplay="autoplay" controls width="98%" height="100%" style="padding-left: 2%;">
													
												</video>
												<!-- <video autoplay="autoplay" width="98%" height="100%" style="padding-left: 2%;">
													<source src="videourl" type="video/mp4"></source>
												</video> -->
											</div>
										</el-row>
										<el-row>
											<el-col :span="12">
												<div class="kuang" style="height: 110px;">
													<video src="videosrc" autoplay="autoplay" controls width="98%" height="100%" style="padding-left: 2%;">
														
													</video>
													<!-- <video autoplay="autoplay" width="98%" height="100%" style="padding-left: 2%;">
														<source src="videourl" type="video/mp4"></source>
													</video> -->
												</div>
											</el-col >
											<el-col :span="12">
												<div class="kuang" style="height: 110px;">
													<!-- <video autoplay="autoplay" width="98%" height="100%" style="padding-left: 2%;">
														<source src="videourl" type="video/mp4"></source>
													</video> -->
													<video src="videosrc" autoplay="autoplay" controls width="98%" height="100%" style="padding-left: 2%;">
														
													</video>
												</div>
											</el-col>
										</el-row>
									</el-col>
									<el-col :span="6">
										<el-row>
											<div class="kuang" style="height: 110px;">
												<!-- <video autoplay="autoplay" muted  width="98%" height="100%" style="padding-left: 2%;">
													<source src="https://img.cdn.aliyun.dcloud.net.cn/guide/uniapp/%E7%AC%AC1%E8%AE%B2%EF%BC%88uni-app%E4%BA%A7%E5%93%81%E4%BB%8B%E7%BB%8D%EF%BC%89-%20DCloud%E5%AE%98%E6%96%B9%E8%A7%86%E9%A2%91%E6%95%99%E7%A8%8B@20200317.mp4" type="video/mp4"></source>
												</video> -->
												<video src="videosrc" muted autoplay="autoplay" controls width="98%" height="100%" style="padding-left: 2%;">
													
												</video>
											</div>
										</el-row>
										<el-row>
											<!-- <div v-for="(item,i) in vedioList" :key="i">
											   <video muted="muted" :id="startvideo+i" class="video" :src="item.path" type="video/mp4" poster="false.png" autoplay="autoplay" controls="controls" loop="-1">
													  <p>你的浏览器不支持video标签.</p>
											   </video>
											</div> -->
											
											<div class="kuang" style="height: 110px;">
												<video  controls="controls" autoplay="autoplay" muted width="98%" height="100%" style="padding-left: 2%;">
													<source src="videosrc" type="video/mp4"></source>
												</video>
											</div>
										</el-row>
										<el-row>
											<div class="kuang" style="height: 110px;">
												<!-- <video autoplay="autoplay" width="98%" height="100%" style="padding-left: 2%;">
													<source src="case2_car.mp4" type="video/mp4"></source>
													
												</video> -->
												<video autoplay="autoplay" controls width="98%" height="100%" style="padding-left: 2%;">
													<source src="video/case2_car.mp4" type="video/mp4"></source>
												</video>
											</div>
										</el-row>
									</el-col>
								</div>
							</el-row>
							<!-- <div class="big_title" style="font-size: 20px;float:left;">
								<span style="text-shadow: .3rem 0 0.3rem #00d8ff;">路口监控</span>
							</div> -->
							
						</div>
					</el-row>
					
				</el-col>
			</el-row>
			<el-row  style="padding-left: 20px;">
				<el-col :span="8">
					<div style="padding-top: 20px;padding-right: 40px;">
						<el-row style="background-color: rgba(22, 31, 38, 0.7);">
							<el-row>
								<div class="titlebox" >
									<span style="font-size: 20px;font-weight:550;color:white;padding-left: 20px;">应急事件进度</span>
								</div>
							</el-row>
							<el-row>
								<template >
								  <div class="block"  style="padding-top: 20px;">
								  <el-timeline>
								    <el-timeline-item timestamp="2023/04/11  11:23:00" placement="top">
										<el-card style="background: transparent;border-color: #6b7179;">
											<div>
												<span style="color: white;">监控摄像头“校门口-东-1”在“校门口检测到“一级警情” : “烟雾明火”,属于“消防告警”类型</span>
											</div>
										</el-card>
								    </el-timeline-item>
									<el-timeline-item timestamp="2023/04/11  11:23:00" placement="top">
										<el-card style="background: transparent;border-color: #6b7179;">
											<div>
												<span style="color: white;">告警属于“消防告警”,已通知“安保部门”,等待相关人员处理！</span>
											</div>
										</el-card>
									</el-timeline-item>
									<el-timeline-item timestamp="2023/04/11  11:23:00" placement="top">
									
									</el-timeline-item>
									
								    
								    
								    
								  </el-timeline>
								</div>
								</template>
								
								
					
							</el-row>
						</el-row>
					</div>
				</el-col>
				<el-col :span="16">
					<div style="padding-top: 20px;"></div>
					<div class="" style="background-color: rgba(22, 31, 38, 0.7);">
						<el-row>
							<div class="titlebox" >
								<span style="font-size: 20px;font-weight:550;color:white;padding-left: 760px;">应急调度</span>
							</div>
						</el-row>
						<el-row :gutter="8" style="padding-top: 20px;padding-left: 5px;">
							<el-col :span="6" >
								<span style="color: white;">校园广播</span>
								<div style="padding-top: 10px;"></div>
								<div class="kuang" >
									<el-row style="padding-top: 15px;">
										<div style="padding-right: 30px;">
											<el-tree :data="treedata" :props="defaultProps" default-expand-all style="padding-left: 20px;padding-top: 10px;padding-bottom: 10px;background-color: transparent;color:white"></el-tree>
										</div>
									</el-row>

								</div>
							</el-col>
							<el-col :span="6" >
								<span style="color: white;">校内安保</span>
								<div style="padding-top: 10px;"></div>
								<div class="kuang" >
									<el-table
									class="customer-no-border-table"
									      :data="tableData2"
									      style="padding-top: 8px;text-align: center;height:100%;zoom:0.8"
										  :header-cell-style="{color: 'white', fontSize: '14px', backgroundColor: '#033353',}">
									      <el-table-column
									        prop="trainname"
									        label="姓名"
											align="center"
											>
									      </el-table-column>
									      <el-table-column
									        prop="modelname"
									        label="联系电话"
											align="center"
											width="120px">
									      </el-table-column>
									      <el-table-column
									        prop="dataname"
									        label="区域"
											align="center"
											width="60px"
											>
									      </el-table-column>
										 
									    </el-table>
								</div>
							</el-col>
							<el-col :span="6">
								<span style="color: white;">周边警力</span>
								<div style="padding-top: 10px;"></div>
								<div class="kuang" >
									<el-table
									class="customer-no-border-table"
									      :data="tableData1"
									      style="padding-top: 8px;text-align: center;height:100%;zoom:0.8"
										  :header-cell-style="{color: 'white', fontSize: '14px', backgroundColor: '#033353',}">
									      <el-table-column
									        prop="trainname"
									        label="派出所"
											align="center"
											>
									      </el-table-column>
									      <el-table-column
									        prop="modelname"
									        label="在岗"
											align="center">
									      </el-table-column>
									      <el-table-column
									        prop="dataname"
									        label="距离"
											align="center">
									      </el-table-column>
										 
									    </el-table>
								</div>
							</el-col>
							<el-col :span="6">
								<span style="color: white;">应急车辆</span>
								<div style="padding-top: 10px;"></div>
								<div class="kuang" >
									<el-table
									class="customer-no-border-table"
									      :data="tableData3"
									      style="padding-top: 8px;text-align: center;height:100%;zoom:0.8"
										  :header-cell-style="{color: 'white', fontSize: '14px', backgroundColor: '#033353',}">
									      <el-table-column
									        prop="trainname"
									        label="类型"
											align="center"
											>
									      </el-table-column>
									      <el-table-column
									        prop="modelname"
									        label="单位"
											align="center"
											>
									      </el-table-column>
									      <el-table-column
									        prop="dataname"
									        label="可调用量"
											align="center"
											
											>
									      </el-table-column>
										 
									    </el-table>
								</div>
							</el-col>
							
						</el-row>
						<!-- <div class="big_title" style="font-size: 20px;float:left;">
							<span style="text-shadow: .3rem 0 0.3rem #00d8ff;">路口监控</span>
						</div> -->
						
					</div>
				</el-col>
									
								</el-row>
			
			
			
		</div>
	</div>
	
</template>

<script>
	 // import 'video.js/dist/video-js.css'
	// import { videoPlayer } from 'vue-video-player'
	
	// import 'video.js/dist/video-js.css'
	
	export default {
		components: {
		  // videoPlayers
		},
		data() {
			return {
				videosrc:require('@/assets/video/case2_car.mp4'),
				// videourl:require('../assets/video/case2_car.mp4'),
				
				playerOptions: {
				                playbackRates: [0.5, 1.0, 1.5, 2.0], // 可选的播放速度
				                autoplay: false,  // 如果为true,浏览器准备好时开始回放
				                muted: false,     // 默认情况下将会消除任何音频。
				                loop: false,      // 是否视频一结束就重新开始。
				                preload: 'auto',  // 建议浏览器在<video>加载元素后是否应该开始下载视频数据。auto浏览器选择最佳行为,立即开始加载视频（如果浏览器支持）
				                language: 'zh-CN',
				                aspectRatio: '16:9',  // 将播放器置于流畅模式，并在计算播放器的动态大小时使用该值。值应该代表一个比例 - 用冒号分隔的两个数字（例如"16:9"或"4:3"）
				                fluid: true,  // 当true时，Video.js player将拥有流体大小。换句话说，它将按比例缩放以适应其容器。
				                sources: [{
				                    type: "video/mp4",  // 类型
									src: require('@/assets/video/case2_car.mp4'),
				                    // src:'',// url地址
				                }],
				                poster: '',  // 封面地址
				                notSupportedMessage: '此视频暂无法播放，请稍后再试',  // 允许覆盖Video.js无法播放媒体源时显示的默认信息。
				                controlBar: {
				                    timeDivider: true,           // 当前时间和持续时间的分隔符
				                    durationDisplay: true,       // 显示持续时间
				                    remainingTimeDisplay: false, // 是否显示剩余时间功能
				                    fullscreenToggle: true       // 是否显示全屏按钮
				                }
				            },
				
				
				
				treedata:[
						{
							label: '图安校园',
							children:[
								{
									label:"教学区",
									children:[{
										label:"北楼",
										
									},{
										label:"南楼",
										
									},
									]
									
								},
								{
									label:"宿舍区",
									children:[{
										label:"一区",
										
									},
									{
										label:"二区",
										
									}]
									
								},
								{
									label:"体育馆",
									
								},
								
							]}],
				
				// 告警事件详情
				form:{
						  id:'1',
						  status:'处理中',
						  alarmLevel:'一级警情',
						  alarmType:"消防告警",
						  alarmName:'烟雾明火',
						  detectionId:'停车场-西-1',
						  alarmArea:'停车场',
						  alarmTime:'2023-04-01 11:23:11',
						  alarmper:"70%",
						  alarmjgtime:'20s',
						  alarmvediourl:"https://img.cdn.aliyun.dcloud.net.cn/guide/uniapp/%E7%AC%AC1%E8%AE%B2%EF%BC%88uni-app%E4%BA%A7%E5%93%81%E4%BB%8B%E7%BB%8D%EF%BC%89-%20DCloud%E5%AE%98%E6%96%B9%E8%A7%86%E9%A2%91%E6%95%99%E7%A8%8B@20200317.mp4",
						  alarmdept:'安保部门',
						  alarmperson:'维修工1',
						  alarmres:'处理完成',
				},
				
				//告警时间进度
						approvalProcessProject:[
						   {id:'0',label: " 告警检测"},
						   { id:'1',label: "告警通知"},
						   { id:'2',label: "告警处理"},
						   
				],
				
				tableData1: [{
				  	            trainname: '光明派出所',
				  	            modelname: '20',
				  	            dataname: '3000m',
				  	          },
							  {
								trainname: '黎明派出所',
								modelname: '20',
								dataname: '4243m',
							  },
							  {
									trainname: '光明派出所',
									modelname: '20',
									dataname: '4243m',
								  },
							  {
								trainname: '黎明派出所',
								modelname: '20',
								dataname: '4243m',
							  },
							  {
							  									trainname: '光明派出所',
							  									modelname: '20',
							  									dataname: '4243m',
							  								  },
							  {
							  								trainname: '黎明派出所',
							  								modelname: '20',
							  								dataname: '4243m',
							  },
				  			  
				  			
				  			],
			tableData2: [{
			  	            trainname: '李一文',
			  	            modelname: '17853942650',
			  	            dataname: '南门',
			  	          },
						  {
							trainname: '王强',
							modelname: '17853942650',
							dataname: '南门',
						  },
						  {
								trainname: '李一文',
								modelname: '17853942650',
								dataname: '南门',
							  },
						  {
							trainname: '王强',
							modelname: '17853942650',
							dataname: '南门',
						  },
						  {
						  									trainname: '李一文',
						  									modelname: '17853942650',
						  									dataname: '南门',
						  								  },
						  {
						  								trainname: '王强',
						  								modelname: '17853942650',
						  								dataname: '南门',
						  },
			  			  
			  			
			  			],
			tableData3:[
				{
					trainname: '救护车',
					modelname: '人民医院',
					dataname: '5',
				},
				{
					trainname: '救护车',
					modelname: '光明医院',
					dataname: '5',
				},
				{
					trainname: '消防车',
					modelname: '人民消防站',
					dataname: '5',
				},
				{
					trainname: '消防车',
					modelname: '光明消防站',
					dataname: '5',
				},
				{
					trainname: '警车',
					modelname: '光明派出所',
					dataname: '5',
				},{
					trainname: '警车',
					modelname: '人民派出所',
					dataname: '5',
				},
			],
								
								
				
				  					
				  	
				
				newTime: "",
				 // vedioList: [{ path: "/video/case2_car.mp4" }, { path:         
				 //             "/webm/CAMERAV.webm" },
				 //            { path: "/video/case2_car.mp4" }, { path: 
				 //             "/webm/CAMERAV.webm" }],
				 
				 // playerOptions: {
				 
				 //                     playbackRates: [0.7, 1.0, 1.5, 2.0], //播放速度
				 
				 //                     autoplay: false, //如果true,浏览器准备好时开始回放。
				 
				 //                     controls: true, //控制条
				 
				 //                     preload: 'auto', //视频预加载
				 
				 //                     muted: false, //默认情况下将会消除任何音频。
				 
				 //                     loop: false, //导致视频一结束就重新开始。
				 
				 //                     language: 'zh-CN',
				 
				 //                     aspectRatio: '16:9', // 将播放器置于流畅模式，并在计算播放器的动态大小时使用该值。值应该代表一个比例 - 用冒号分隔的两个数字（例如"16:9"或"4:3"）
				 
				 //                     fluid: true, // 当true时，Video.js player将拥有流体大小。换句话说，它将按比例缩放以适应其容器。
				 
				 //                     sources: [{
				 
				 //                         type: 'video/mp4',
				 
				 //                         src: 'src/views/video/case2_car.mp4'
				 
				 //                         //src: 'src/views/sjsc/sjsc01_carInfoManage/2.mp4'//你所放置的视频的地址，最好是放在服务器上
				 
				 //                     }],
				 
				 //                     //poster: "http://39.106.117.192:8080/static/indexImg.png", //你的封面地址（覆盖在视频上面的图片）
				 
				 //                     width: document.documentElement.clientWidth,
				 
				 //                     notSupportedMessage: '此视频暂无法播放，请稍后再试' //允许覆盖Video.js无法播放媒体源时显示的默认信息。
				 
				 //            },
							 
				// playerOptions: {
				//           height: '360',
				//           autoplay: true,
				//           muted: true,
				//           language: 'en',
				//           playbackRates: [0.7, 1.0, 1.5, 2.0],
				//           sources: [{
				//             type: "video/mp4",
				//             src: "https://img.cdn.aliyun.dcloud.net.cn/guide/uniapp/%E7%AC%AC1%E8%AE%B2%EF%BC%88uni-app%E4%BA%A7%E5%93%81%E4%BB%8B%E7%BB%8D%EF%BC%89-%20DCloud%E5%AE%98%E6%96%B9%E8%A7%86%E9%A2%91%E6%95%99%E7%A8%8B@20200317.mp4",
				//           }],
				//           poster: "https://surmon-china.github.io/vue-quill-editor/static/images/surmon-1.jpg",
				//         }

			}
		},
		mounted(){
		        this.getNowTime();//进入页面调用该方法获取当前时间
		        clearInterval(myTimeDisplay );//销毁之前定时器
		        var myTimeDisplay = setInterval(() => {
		           this.getNowTime(); //每秒更新一次时间
		        }, 1000);  
				
				for (var i = 0; i < 4; i++) {
				        //获取四个视频的id
				            var video = document.getElementById("startvideo"+i);
				        //调用video标签的播放函数
				            video.play();
				        }
		},
		methods: {
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
			
		},
	}
</script>

<style lang="scss">
	
	
	.physical-video .video-js.vjs-custom-skin {
	  height: 100vh;
	}
	.physical-video .video-js.vjs-custom-skin .vjs-control-bar {
	  height: 90px;
	}
	.physical-video .video-js.vjs-custom-skin .vjs-control {
	    width: 4em!important;
	}
	.physical-video .video-js .vjs-time-control,.physical-video .video-js.vjs-custom-skin .vjs-control-bar .vjs-playback-rate .vjs-playback-rate-value {
	  font-size: 2em!important;
	  line-height: 3em!important;
	}
	.physical-video .video-js .vjs-control:before {
	  height: 50px;
	  font-size: 4em;
	}
	
.kuang{
	background: url(../assets/images/kuang.png) no-repeat;
	background-size: 100% 100%;
}
.kuang6{
	background: url(../assets/images/kuang6.png) no-repeat center;
	background-size: 100% 100%;
	// zoom:1.5;
	overflow: hidden;
	// animation: show5 1s linear forwards 8.5s;
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

	

	.div1{
		
		background: url(../assets/images/kuang2.png) no-repeat;
		background-size: 95% 100%
		/* background-size:400px 668px; */
		/* padding-top: 10px; */
		/* width: 520px;
		height: 300px; */
		/* zoom:1.1 */
	}
	.div-layout{
		height: 900px;
		background-image: url(../assets/images/school.png) ;
		background-size: 1370px 900px;
	}
	
	/*最外层透明*/
	.regional_table ::v-deep .el-table,
	.regional_table ::v-deep .el-table__expanded-cell {
	  background-color: transparent;
	  color: white;
	}
	/* 表格内背景颜色 */
	.regional_table ::v-deep .el-table th,
	.regional_table ::v-deep .el-table tr,
	.regional_table ::v-deep .el-table td {
	  background-color: transparent !important;
	  color: white;
	}
	
	/*最外层透明*/
	.el-table, .el-table__expanded-cell{
	    background-color: transparent;
	}
	/* 表格内背景颜色 */
	.el-table th,
	.el-table tr,
	.el-table td {
		color: white;
	    background-color: transparent;
	}
	
	
	.el-table::before {
		 left: 0;
		 bottom: 0;
		 width: 100%;
		 height: 0px;
	}
	/* .el-table th, .el-table tr {
		color: white;
	    background-color: transparent;
	} */
	
	
	.el-textarea__inner,.el-input__inner {
	    background: transparent !important;
	}
	
	// .el-upload{
	// 	background: transparent !important;
	// }
	
	.upload-demo::v-deep .el-upload,.el-upload--text{
		background: transparent !important;
		
	}
	
	
	.upload-demo ::v-deep .el-upload--picture-card{
	  margin-top: 4%;
	  height:80px;
	  width:80px;
	  line-height: 80px;
	}
	.upload-demo ::v-deep .el-upload-list--picture-card .el-upload-list__item{
	  margin-top: 4%;
	  height:80px;
	  width:80px;
	  line-height: 80px;
	}
	
	

</style>
