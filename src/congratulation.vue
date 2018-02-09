<template>
	<v-ons-page>
		<div class="cong_bg">
			<div class="remove">
				<v-ons-card style="background-color: #e91e63;">
				<p><strong> Fill Up the Form for Better Experience </strong></p>
				</v-ons-card>
				<v-ons-card style="background-color:rgba(233, 30, 99, 0.1);">

					<form>
						<div class="login_form" align="center">
							<i class="zmdi zmdi-graduation-cap" style="color:#fff" size="20"></i>
							<v-ons-input float type="text"  modifier="material"
							placeholder="Academic Qualification" ons-model="full"></v-ons-input>
							<br><br>

							<i class="zmdi zmdi-library" style="color:#fff" size="20"></i>
							<v-ons-input float type="text"  modifier="material"
							placeholder="Discipline" ons-model="user"></v-ons-input>
							<br><br>
							<i class="zmdi zmdi-favorite"  style="color:#fff" size="20"></i>

							<v-ons-input float type="text"  modifier="material"
							placeholder="Preferable Exams" ons-model="email"></v-ons-input>
							<br><br>
							<v-ons-button class="got_it_button"ripple modifier="large" style="margin: 6px 0" @click="dash">Got It</v-ons-button>

						
					</div>
				</form>
			</v-ons-card>
		</div>
	</div>
</v-ons-page>
</template>
<script >

	import customToolbar from './CustomToolbar';
	import dash from './dashboard';

	export default{
		data() {
			return{

			}

		},
		methods:{
			dash(){
				this.pageStack.push(dash);
			}
		},



		props: ['pageStack'],
		components: { customToolbar }
	}
	
</script>
<style>
	.cong_bg{
		background-color: #e91e63;
		position: absolute;

		width: 100%;
		height: 100%;
	}
	p{
		text-align: center;
		color:white;
		font-size: 20px;
		font-weight: 100vh;
		font-family: 'Roboto';

	}
	.remove{
		position: relative;
		top: 50%;
		transform: translateY(-50%);
	}

	

	ons-input .text-input--material{
		color:#fff !important;
	}
	span.text-input--material__label--active
	{
		color:#fff !important; 
	}
	.text-input--material__label{
		color: #fff !important;
	}
	.got_it_button{
		background-color: #D24D57 !important;
		border: 2px solid #fff !important ;
		border-radius:9px !important;
	}


</style>