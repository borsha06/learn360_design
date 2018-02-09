<template>
	<v-ons-page>
		<div class="dash_bg">
			<div class="element" align="center" style=" background-color:#218c74; height=100%">
				<br>

				<strong>Menu</strong>
			</div>

			<div class="section" >
				<v-ons-row class="user_cover">
					<v-ons-col>
						<div class="user" style="background-color:#ff5252"><i id="dash_icon" class="ion-ios-book"></i>
							<div class="time" id="user_2_name"><strong>Subjcts</strong>
							</div>
						</div>



					</v-ons-col>
				</v-ons-row>

				<v-ons-row class="user_cover">
					<v-ons-col>
						<div class="user" style="background-color:#f19066"><i id="dash_icon" class="ion-ios-pulse-strong"></i>
							<div class="time" id="user_2_name"><strong>Exams</strong>
							</div>
						</div>

					</v-ons-col>
				</v-ons-row>





				<v-ons-row class="user_cover">
					<v-ons-col >
						<div class="user" style="background-color: #e17055"><i id="dash_icon" class="ion-android-phone-landscape"></i>
							<div class="time" id="user_2_name"><strong>Tutorials</strong>
							</div>
						</div>
					</v-ons-col>

				</v-ons-row>

				<v-ons-row class="user_cover">
					<v-ons-col >
						<div class="user" style="background-color: #c44569"><i id="dash_icon"class=" ion-ios-pie"></i>
						<div class="time" id="timer_4"><strong>Analysis</strong>
							</div>
						</div>

					</v-ons-col>
				</v-ons-row>

					<v-ons-row class="user_cover">
					<v-ons-col >
						<div class="user" style="background-color: #218c74"><i id="dash_icon"class=" ion-ios-gear"></i>
						<div class="time" id="timer_4"><strong>Settings</strong>
							</div>
						</div>

					</v-ons-col>
				</v-ons-row>
				


			</div>
		</div>
	</v-ons-page>
</template>
<script >

	import customToolbar from './CustomToolbar';
	export default{
		data(){
			return{

			}
		},



		props: ['pageStack'],
		components: { customToolbar }
	}
</script>
<style >
	@import url('https://fonts.googleapis.com/css?family=Nanum+Myeongjo:400,700,800&subset=korean');
	.element {
		animation: pulses 10s infinite;
		height: 70px;
		color: #fff;
		font-size: 25px;
		font-family: 'Helvetica Nue'



	}
	.list-header{
		text-align: center;
		font-size: 30px;
		background-color: #17c0eb;
		color: #fff;
	}

	@keyframes pulses {
		0% {

			background-color: #20bf6b;

		}
		20%{
			background-color: #45aaf2;
		}

		50% {
			background-color: #2bcbba;
		}
		100% {

			background-color: #26de81;
		}
	}

	body,
	html {
		height: 100%;
	}

	body {
		display: flex;
		align-items: center;
		justify-content: center;
	}
	.time {
		text-align: center;
		color: white;
		width: 100%;
		font-size: 22px;
		margin-top: 5px;
	}
	.user_cover{

	}
	.user {
		width:100%;
		height:100%;	
		display: table;
		text-align: center;
		margin: auto;

	}
	.user strong{
		font-family: 'Nanum Myeongjo', serif !important;
	}

	.user ons-icon {
		font-size: 70px;
		display: table-cell;

	}
	.section{

	}
	#dash_icon{
		color: white;
		font-size: 400%;
		align:center;
	}

</style>