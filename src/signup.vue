<template>
  <v-ons-page modifier="bg ">
    <v-ons-card class="cards" style="  position: relative;
    top: 50%;
    transform: translateY(-50%); ">
    <div class="left">
      <v-ons-back-button></v-ons-back-button>
    </div>
    <div class="title" align="center" style="font-family:  'Helvetica Neue';
    font-weight: 200;color:#fff;" >
    <strong>
      Sign Up
    </strong>
  </div>
  <br>
  <form>
   <div class="login_form" align="center">

     <v-ons-icon size="20px" icon ="md-account" style="color:#fff"></v-ons-icon>
     <v-ons-input float type="text"  modifier="material"
     placeholder="Fullname" ons-model="full"></v-ons-input>
     <br><br>

     <v-ons-icon size="20px" icon ="md-face" style="color:#fff"></v-ons-icon>
     <v-ons-input float type="text"  modifier="material"
     placeholder="Username" ons-model="user"></v-ons-input>
     <br><br>
     <v-ons-icon size="20px" icon="md-email" style="color:#fff"></v-ons-icon>

     <v-ons-input float type="text"  modifier="material"
     placeholder="Email" ons-model="email"></v-ons-input>
     <br><br>
     <v-ons-icon size="20px" icon="md-phone" style="color:#fff"></v-ons-icon>

     <v-ons-input float type="text"  modifier="material"
     placeholder="Mobile" ons-model="mobile"></v-ons-input>
     <br><br>
     <v-ons-icon size="20px" icon="md-lock" style="color:#fff"></v-ons-icon>

     <v-ons-input float type="password"  modifier="material"
     placeholder="Password" ons-model="pass"></v-ons-input>
     <br><br>
     <v-ons-button ripple style="margin: 6px 0" >Sign Up

     </v-ons-button>
   </div>


 </div>
</form>

</div>


</div>
</v-ons-col>
</v-ons-row>

</form>
</v-ons-card>
</v-ons-page>
</template>

<script>
  import customToolbar from './CustomToolbar';

  export default {
    data(){
      return {
        full: "",
        user:"",
        email:"",
        mobile:"",
        pass: "",
      }

    },
    methods: {
      pop() {
        this.pageStack.pop();
      }, 
    },
    props: ['pageStack'],
    components: { customToolbar }
  }
</script>
<style scoped>
  .page__background{
    background-image:url('../www/assets/img10.jpg ' ) !important;
  }
  .card{
    padding: 20px;
    background: rgba(255,255,255,0.1) !important;
    border-radius: 8px !important; 
  }

  .button{
    background-color: #3244cc;
    font-family: 'Helvetica Neue';
  }
  
  .left{
    width: 1%;


  }

  ons-back-button .back-button__icon.back-button--material__icon{
    fill: #ffffff !important;
  }
  ons-input .text-input--material{
    color:#eae8e9 !important;
  }
  span.text-input--material__label--active{
    color:#fff !important; 
    text-decoration: none !important;
  }
</style>