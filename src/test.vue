<template>
	<v-ons-page>
		<div class="test_body" >
			<v-ons-card style="text-align:center; background-color:#e74c3c;  position: relative;
			top: 50%;
			transform: translateY(-50%); ">
			
			<div class="timer">
				<div class="minutes" v-text="minutes"></div>
				<div class="seconds" id="seconds" v-text="secondsShown"></div>
			</div>
			<h1 align="center" class="text"><strong>{{ title }}</strong></h1>
			<div v-for="(question,index) in questions">
				<div v-show="index === ques_index">
				<p class="header_text" >{{ question.header }} </p>

					<ul align= "left">
						<li   v-for="response in question.responses">
							<label>

								<input type="radio" 
								v-bind:value=" response.correct " 
								v-bind:name="index" 
								v-model="choices[index]"> <strong>{{ response.text }}</strong>
							</label>
						</li>
					</ul>
					<v-ons-button class="prev_next_button"modifier="cta" style="margin: 6px 0" v-if="ques_index > 0" @click="prev">
						Prev
					</v-ons-button>

					<v-ons-button  class="prev_next_button" modifier="cta" style="margin: 6px 0" @click="next">
						Next
					</v-ons-button>
				</div>
			</div>

			<div v-show="ques_index === questions.length" >
				
				<h2>
					Quiz finished
				</h2>
				<p>
					Total score: {{ score() }} / {{ questions.length }}
				</p>

<v-ons-button class="prev_next_button" modifier="cta" style="margin: 6px 0" @click="congratz">
						Congratulation
					</v-ons-button>
			</div>




		</v-ons-card>
	</div>

</v-ons-page>
</template>
<script >
	import customToolbar from './CustomToolbar';
	
	import swal from  'sweetalert';
	import congratz from './congratulation'
	export default{

		data(){
			return{
				minutes: 2,
				seconds: 0,
				interval: null,
				started: true,
				title: "2 minutes quiz",

				questions: [
				{
					header:'What is the Capital of Bangladesh?',
					responses: [
					{ text: 'Dinajpur' }, 
					{ text: 'Dhaka', correct: true }
					]
					

				},
				{
					header:'What is the Capital of USA?',
					
					responses: [
					
					{ text: 'New York' }, 
					{ text: 'Washington DC', correct: true }
					]
					

				},

				{header:'Who is the founder of Facebook',
				responses: [{text:'Bill Gates'},
				{text:'Mark Zuckerberg',correct: true}
				]
			},
			{
				header:'Who is the founder of SpaceX',
				responses:[
				{text:'Mark Zuckerberg'},
				{text:'Elon Musk',correct:true}]

			},

				],
				
				
				ques_index: 0,
				choices: Array(4).fill(false)
			}
		},
		mounted(){
			this.loaded()
		},
		methods:{
			congratz(){
				 swal({
      text: "Congratulation on Your First Exam!",
    });
				this.pageStack.push(congratz)
			},
			next: function() {
				this.ques_index++;
			},

			prev: function() {
				this.ques_index--;
			},

			score: function() {
				return this.choices.filter(function(val) { return val }).length;
			},
			loaded: function() {
				this.interval = setInterval(this.intervalCallback, 1000)
			},
			


			intervalCallback: function() {
				if(!this.started) return false
					if(this.seconds == 0) {
						if(this.minutes == 0) {
							return null
						}
						this.seconds = 59
						this.minutes--
					} else {
						this.seconds--
					}
				}

			},
			computed: {
				timeouts: function() {
					if(this.ques_index === this.questions.length){
						console.log(this.ques_index)
						this.started = false
					}
					return this.seconds

				},
				secondsShown: function() {
					if(this.seconds < 10) {
						return "0" + parseInt(this.seconds, 10)
					}
					return this.seconds
				},
			},


			

			props: ['pageStack'],
			components: { customToolbar }
		}
	</script>
	<style >

		.test_body{
			background-color: #c0392b;
			position: absolute;
			width: 100%;
			height: 100%;
			float: left;
			color:white;

		}
		.timer {
			display: flex;
			color: white;
			margin: 0 auto;
			font-size: 16vh;
			justify-content: center;
			font-weight: 700;
			text-shadow:1px 3px 0 #3A6073,
			1px 8px 0 #16222A,


		}

		.seconds::before {
			content: ":";	
			/*display:block;*/
			font-size: 16vh	;
			font-weight: 700;		
			z-index: 999;
			/*position: absolute;	*/
			margin-bottom: -15px
		}


		body {
			display: flex;
			height: 100%;
			align-items: center;
			justify-content: center;
		}

		.header_text{
			font-weight: 700vh;
			font-family: 'Roboto';
			font-size: 30px;
			text-align: center;
			color: white;



		}

		.text{
			font-size: 40px;
		}
		li
		{
			list-style: none;
		}
/*.button--cta{
background-color: #f44336 !important;
border: 2px solid #fff !important ;
border-radius:9px !important;
}
.button.button--material{
	background-color: #f44336 !important;
border: 2px solid #fff !important ;
border-radius:9px !important;	
}
*/
.prev_next_button{
		background-color: #f44336 !important;
border: 2px solid #fff !important ;
border-radius:9px !important;

}

	</style>





