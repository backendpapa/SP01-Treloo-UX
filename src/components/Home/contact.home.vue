<template>
  <div class="contact-container">
      <v-row align="center" justify="center" >
          <v-col cols="12" xl="6" lg="6" class="" style="position:relative">
              <p class="font-2 weight-600 d-flex d-sm-none text-center ">Travel Any Corner of The World With Us</p>
             
              <v-img eager src="../../assets/images/contact.png"></v-img>
               <div style="" class="box box-1">
                   <p class="mb-n1 font-3 blue--text weight-600 text-center">300+</p>
                   <p class="font-7 font-weight-light text-center mt-n2">DESTINATIONS</p>
              </div>
              <div style="" class="box box-2">
                   <p class="mb-n1 font-3 blue--text weight-600 text-center">150+</p>
                   <p class="font-7 font-weight-light text-center mt-n2">HOTELS</p>
              </div>
               <div style="" class="box box-3">
                   <p class="mb-n1 font-3 blue--text weight-600 text-center">5000+</p>
                   <p class="font-7 font-weight-light text-center mt-n2">TOURISTS</p>
              </div>
          </v-col>
           <v-col cols="12" xl="6" lg="6" class="">
              <p class="font-2 weight-600 d-none d-sm-flex">Travel Any Corner of The World With Us</p>
              <p class="font-5 font-weight-light">Would you explore nature paradise in the world, let’s find the best destination in world with us, Would you explore nature paradise in the world, let’s find the best destination in world with us. Would you explore nature paradise in the world, let’s find the best destination in world with us.</p>
              <br>
              <p class="font-5 font-weight-light">Would you explore nature paradise in the world, let’s find the best destination in world with us.</p>
              <v-btn large color="blue" style="text-transform:none" class="font-7 font-weight-light" dark>Contact Us</v-btn>
          </v-col>
      </v-row>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.contact-container{
    padding: 4%;
}
.box{
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    height:13vh;
    min-width:100px;
    width: 150px;
    border-radius: 25px !important;
    position:absolute;
    background: white;
    padding-top: 2%;
    
}
.box-1{
    top:15%;
    right: -5%;
}
.box-2{
    top:85%;
    right: -5%;
}
.box-3{
    top:75%;
    left: -5%;
}
@media screen and (max-width:600px) {
    .contact-container{
        padding: 10%;
    }
    .box{
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    height:7vh;
    min-width:100px;
    width: 100px;
    border-radius: 20px !important;
    position:absolute;
    background: white;
    padding-top: 2.5%;
    
}
    .box-1{
    top:35%;
    right: -5%;
}
.box-2{
    top:80%;
    right: -5%;
}
.box-3{
    top:75%;
    left: -5%;
}
}
</style>