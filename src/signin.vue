<template>
  <v-ons-page  >
    <div class="signin">
      <v-ons-card class="cards" style=" position: relative;
      top: 50%;
      transform: translateY(-50%);">
      <div class="title" align="center">
        <strong>
          Sign In
        </strong>

      </div>
      <br>

      <div class="login_form" align="center">
       <form>
        <v-ons-icon size="20px" icon ="md-face" style="color:#fff"></v-ons-icon>

        <v-ons-input float type="text"  modifier="material"
        placeholder="username" ons-model="user"></v-ons-input>
        <br><br>
        <v-ons-icon size="20px" icon="md-lock" style="color:#fff"></v-ons-icon>

        <v-ons-input float type="password"  modifier="material"
        placeholder="password" ons-model="pass" ></v-ons-input>
        <br><br>
        <p  class="signin_text" align="right"  @click="">Forgot <strong> Password?</strong></p>
        <div class="submit" align="center">


          <v-ons-button  ripple  style="margin: 6px 0" @click="sign_in">Sign In

          </v-ons-button>
        </div>


      </form>


    </div>


    <div class="">

      <div align="right" >
        <p align="right" class="signin_text"> Don't have an account? <p align="right" class="signin_text" @click="signup"><strong>Sign up</strong> </p></p>
      </div>

    </div>

  </v-ons-card>
</div>
</v-ons-page>
</template>

<script scoped>
  import customToolbar from './CustomToolbar';
  import signup from './signup';
  import swal from 'sweetalert';
  import welcome from './welcome';
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
   sign_in(){
     swal({
      text: "Let's Have a Quick Test",
    });
     this.pageStack.push(welcome);

   }
 },
 props: ['pageStack'],
 components: { customToolbar }
}
</script>
<style scoped>
  .signin{
    background-image:url('./assets/img10.jpg')!important;
    position: absolute;
    width: 100%;
    height: 100%;
  }

  .card {
    padding: 20px;
    background: rgba(255,255,255,0.15) !important;

  } 

  .signin_text
  {
    font-size: 15px;
    font-family:'Helvetica Neue';
    font-variant:  historical-ligatures;
    color: #fff;

  }
  .button
  {
    background-color: #3244cc;
    font-family: 'Helvetica Neue';
  }
  ons-input .text-input--material{
    color:#eae8e9 !important;
  }
  span.text-input--material__label--active
  {
    color:#fff !important; 
  }
  .title{

    font-family: 'Helvetica Neue';
    font-weight: 200;
    color:#fff;
  }
  .swal-overlay {
    background-color: rgba(31, 78, 105, 0.7);
  }
  .swal-text{
    text-align: center;
  }


</style>