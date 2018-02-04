<template>
	<v-ons-page class="new">
	
	
	<v-ons-list style=" position: relative;
    top: 50%;
    transform: translateY(-50%);" >
	
	<v-ons-list-item  tappable class="timer" modifier="nodivider" v-for="t in timer " >{{t}}
	</v-ons-list-item>
	
	
</v-ons-list>


	</v-ons-page>

</template>
<script>
	export default {
		data(){
			return{
			timer:["2 Minutes","5 Minutes"
				,"10 Minutes","15 Minutes"
			]
		}
		},
	}
</script>
<style>

.timer{
	color: #fff;
	height: 100%;
	width: 100%;
	text-align: center;

}

.new{
background-color: blue;

}
.list{
	background-color:rgba(255,255,255,0.15);
}




</style>