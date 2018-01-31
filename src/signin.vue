<template>
  <v-ons-page modifier="bg ">

    <v-ons-card class="cards" style="  position: relative;
    top: 50%;
    transform: translateY(-50%); ">
    <div class="title" align="center" style="font-family: 'Helvetica Neue';
    font-weight: 200;color:#3244cc;" >
    Sign In 
  </div>
  <br>
  <form>
   <div class="login_form" align="center">
    <v-ons-icon size="20px" icon ="md-face" style="color:indigo"></v-ons-icon>

    <v-ons-input float type="text"  modifier="material"
    placeholder="username" ons-model="user"></v-ons-input>
    <br><br>
    <v-ons-icon size="20px" icon="md-lock" style="color:indigo"></v-ons-icon>

    <v-ons-input float type="password"  modifier="material"
    placeholder="password" ons-model="pass" ></v-ons-input>
    <br><br>
    <p align="right" class="text" style="
    font-size: 14px;
    font-family: cursive;
    font-style:  oblique;
    font-variant:  historical-ligatures;">
    <p align="right" class="text" @click=""><strong>Forgot Password?</strong></p>
    <div class="submit" align="center">


      <v-ons-button  ripple  style="margin: 6px 0" >Sign In

      </v-ons-button>
    </div>



  </div>
</form>

<div class="">

  <div align="right" >
    <p align="right" class="text"> <strong>Don't have an account? </strong><p align="right" class="text" @click="signup"><strong>Sign up</strong> </p></p>
  </div>

</div>
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
  import signup from './signup';
  export default {
    data() {
     return {
      user:"",
      pass:"",
     }
   },
   methods: {
    signup() {
     this.pageStack.push(signup);
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
  .cards{
    z-index:99;
  }
  .card {
   background-color: #ffffff57;
 } 
 .login_form{
  z-index: 99;
}
.text
{
  font-size: 15px;
  font-family: cursive;
  font-style:  italic;
  font-variant:  historical-ligatures;
  color: #0D47A1;

}
.button
{
      background-color: #3244cc;
      font-family: 'Helvetica Neue';
}
</style>