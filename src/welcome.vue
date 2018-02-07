<template>
	<v-ons-page >

		<div class="new">
		<!--
			<div class="square"  v-for="t in timer ">
				<div class="content">
				  {{t}}
				</div>
			</div>
    -->
<br>
    <div class="top" align="center">
     <strong>Hey There,</strong> 
    </div>
    <br><br>
    <div class="top_text">
      <strong>Just Take Your Time and Click Any of the Timer </strong>
    </div>
    </br>
    <div class="section" @click="exams">
    <v-ons-row class="user_cover">
      <v-ons-col>
        <div class="user_thumbnail" style="background-color: #dd6218"><ons-icon icon="fa-clock-o"></ons-icon></div>
        <div class="timer" id="user_2_name"><strong>2 Minutes</strong></div>
      </v-ons-col>
      <v-ons-col >
        <div class="user_thumbnail" style="background-color: #00a899"><ons-icon icon="fa-clock-o"></ons-icon></div>
        <div class="timer" id="user_2_name"><strong>5 Minutes</strong></div>
      </v-ons-col>
    </v-ons-row>
    <v-ons-row class="user_cover">
      <v-ons-col >
        <div class="user_thumbnail" style="background-color: #e3aa05"><ons-icon icon="fa-clock-o"></ons-icon></div>
        <div class="timer" id="user_2_name"><strong>10 Minutes</strong></div>
      </v-ons-col>
      <v-ons-col >
        <div class="user_thumbnail" style="background-color: #94b052"><ons-icon icon="fa-clock-o"></ons-icon></div>
        <div class="timer" id="timer_4"><strong>15 Minutes</strong></div>
      </v-ons-col>
    </v-ons-row>
    </div>
  
  </div>
</v-ons-page>

</template>
<script>
  import customToolbar from './CustomToolbar';
  import swal from  'sweetalert';
  import test from './test';
  export default {
    data(){
     return{
      timer:["2 Minutes","5 Minutes"
      ,"10 Minutes","15 Minutes"
      ]
    }
  },
  methods: {

    exams()
    {
    	this.pageStack.push(test);
    }

  },
  props: ['pageStack'],
  components: { customToolbar }
}
</script>
<style scoped>

	.new{
		background-color: #e74c3c;
		position: absolute;
		width: 100%;
		height: 100%;
		float: left;

	}
	.list{
		background-color:rgba(255,255,255,0.15);
	}

	.square {
		position: relative;
		width: 20%;
		border: 5px solid red;
		text-align: center;
   margin: 20px;
   line-height: 9;
   vertical-align: middle;
 }

 .square:after {
  content: "";
  display: block;
  padding-bottom: 70%;
}
.square.hover{
  border: 7px solid #fff;
}

.content {
  position: absolute;
  width: 100%;
  height: 100%;
}

.user_cover {
  padding: 0px 40px;
  margin: 20px 0px;
}

.timer {
  text-align: center;
  color: white;
  width: 100%;
  font-size: 22px;
  margin-top: 5px;
}

.user_thumbnail {
  width: 100px;
  height: 100px;
  display: table;
  text-align: center;
  margin: auto;
}

.user_thumbnail ons-icon {
  font-size: 70px;
  display: table-cell;
  vertical-align: middle;
}
.top{
  font-weight: 70vh;
  font-size:60px;
  color: white;
  font-family: 'Roboto';
}
.top_text{
  font-weight: 20vh;
  font-size: 20px;
  color:white;
  font-family: 'Helvetica Neue';
  text-align: center;
}

</style>