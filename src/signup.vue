<template>
  <v-ons-page modifier="bg ">
    <v-ons-card class="cards" style="  position: relative;
    top: 50%;
    transform: translateY(-50%); ">
    <div class="left">
      <v-ons-back-button>Sign in</v-ons-back-button>
    </div>
    <div class="title" align="center" style="font-family:  'Helvetica Neue';
    font-weight: 200;color:#3244cc;" >
    Sign Up
  </div>
  <br>
  <form>
   <div class="login_form" align="center">
     <v-ons-icon size="20px" icon ="md-face" style="color:indigo"></v-ons-icon>

     <v-ons-input float type="text"  modifier="material"
     placeholder="Fullname" ons-model="full"></v-ons-input>
     <br><br>
     <v-ons-icon size="20px" icon ="md-account" style="color:indigo"></v-ons-icon>

     <v-ons-input float type="text"  modifier="material"
     placeholder="Username" ons-model="user"></v-ons-input>
     <br><br>
     <v-ons-icon size="20px" icon="md-email" style="color:indigo"></v-ons-icon>

     <v-ons-input float type="text"  modifier="material"
     placeholder="Email" ons-model="email"></v-ons-input>
     <br><br>
     <v-ons-icon size="20px" icon="md-phone" style="color:indigo"></v-ons-icon>

     <v-ons-input float type="text"  modifier="material"
     placeholder="Mobile" ons-model="mobile"></v-ons-input>
     <br><br>
     <v-ons-icon size="20px" icon="md-lock" style="color:indigo"></v-ons-icon>

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
<style>
  .page--bg__background{
    background-image:url('../www/assets/img10.jpg ' );
  }
  .card{
    padding: 37px;
    background-color: #ffffff57;
  }

  .button
  {
    background-color: #3244cc;
    font-family: 'Helvetica Neue';
  }
  .back-button
  { color: #3752cc;
  }

.back-button__icon {
fill: #3752cc;
}
</style>