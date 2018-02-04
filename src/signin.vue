<template>
  <v-ons-page >

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
    <p align="right" class="text" style="
    font-size: 14px;
    font-family: cursive;
    font-style:  oblique;
    font-variant:  historical-ligatures;">
    <p align="right" class="text" @click="">Forgot <strong> Password?</strong></p>
    <div class="submit" align="center">


      <v-ons-button  ripple  style="margin: 6px 0" @click="sign_in">Sign In

      </v-ons-button>
    </div>


  </form>


</div>


<div class="">

  <div align="right" >
    <p align="right" class="text"> Don't have an account? <p align="right" class="text" @click="signup"><strong>Sign up</strong> </p></p>
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
  text: "Let's have a quick test",
});
 this.pageStack.push(welcome);

   }
 },
 props: ['pageStack'],
 components: { customToolbar }
}
</script>
<style>
  .page__background{
    background-image:url('../www/assets/img10.jpg')!important;
  }
 
  .card {
    padding: 20px;
    background: rgba(255,255,255,0.15) !important;

 } 

 .text
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