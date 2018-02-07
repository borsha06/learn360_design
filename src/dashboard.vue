<template>
	<v-ons-page>
	<v-ons-card cstyle="background-color:#C0392B;">
	<strong>Welcome to the Dashboard</strong>

	</v-ons-card>
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
<style ></style>