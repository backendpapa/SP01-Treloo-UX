<template>
  <div class="ts-container">
      <v-row >
          <v-col cols="12" xl="6" lg="6">
              <v-card style="position:relative" flat class="te-card white">
                   <div style="position:absolute;top:0;width:80%">
                         <p  style="font-size:250px;text-align:center;opacity:0.3" class="grey--text">"</p>
                 </div>
                 <v-row align="center" justify="center" style="height:100%">
                     <div>
                          <p class="font-5 text-center mb">Our trip to Morocco was truly a onece in a lifetime experience and we are so grateful to everyone that made it happen seamlessly. Our travel planner, Jaouad, was increadible.</p>
                          <p class="blue--text font-5 text-center ">-Vand D</p>
                          <p class="grey--text font-5 text-center mb-n1">Happy Treloo</p>
                     </div>
                 </v-row>
                 <div class="" style="position:absolute;bottom:-12%;width:80%">
                     <v-row no-gutters>
                         <v-spacer></v-spacer>
                         <v-avatar class="d-none d-sm-flex" size="120"  color="white">
                            <v-avatar size="90">
                                 <v-img eager src="https://images.unsplash.com/photo-1531746020798-e6953c6e8e04?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxleHBsb3JlLWZlZWR8OHx8fGVufDB8fHx8&auto=format&fit=crop&w=800&q=60"></v-img>
                            </v-avatar>
                            <v-chip style="position:absolute;top:20%;right:5%;z-index:1" color="white" class="weight-600" x-small    ><v-rating class="ml-n2" color="yellow darken-1" length="1" x-small dense value="1" v-model="rating"></v-rating> 5.5</v-chip>
                         </v-avatar>
                         <v-avatar class="d-flex d-sm-none" size="60"  color="white">
                            <v-avatar size="40">
                                 <v-img eager src="https://images.unsplash.com/photo-1531746020798-e6953c6e8e04?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxleHBsb3JlLWZlZWR8OHx8fGVufDB8fHx8&auto=format&fit=crop&w=800&q=60"></v-img>
                            </v-avatar>
                         </v-avatar>
                         <v-spacer></v-spacer>
                     </v-row>
                 </div>
                
                
              </v-card>
          </v-col>
           <v-col cols="12" xl="6" lg="6">
              <v-card style="position:relative" flat class="te-card white">
                   <div style="position:absolute;top:0;width:80%">
                         <p  style="font-size:250px;text-align:center;opacity:0.3" class="grey--text">"</p>
                 </div>
                 <v-row align="center" justify="center" style="height:100%">
                     <div>
                          <p class="font-5 text-center mb">Our trip to Morocco was truly a onece in a lifetime experience and we are so grateful to everyone that made it happen seamlessly. Our travel planner, Jaouad, was increadible.</p>
                          <p class="blue--text font-5 text-center ">-Vand D</p>
                          <p class="grey--text font-5 text-center mb-n1">Happy Treloo</p>
                     </div>
                 </v-row>
                 <div class="" style="position:absolute;bottom:-12%;width:80%">
                     <v-row no-gutters>
                         <v-spacer></v-spacer>
                         <v-avatar class="d-none d-sm-flex" size="120"  color="white">
                            <v-avatar size="90">
                                 <v-img eager src="https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80"></v-img>
                            </v-avatar>
                            <v-chip style="position:absolute;top:20%;right:5%;z-index:1" color="white" class="weight-600" x-small    ><v-rating class="ml-n2" color="yellow darken-1" length="1" x-small dense value="1" v-model="rating"></v-rating> 5.5</v-chip>
                         </v-avatar>
                         <v-avatar class="d-flex d-sm-none" size="60"  color="white">
                            <v-avatar size="40">
                               
                                 <v-img eager src="https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80"></v-img>
                            </v-avatar>
                             
                         </v-avatar>
                         <v-spacer></v-spacer>
                     </v-row>
                 </div>
                
                
              </v-card>
          </v-col>
      </v-row>
  </div>
</template>

<script>
export default {
    data(){
        return {
            rating:1
        }
    }
}
</script>

<style>
.ts-container{
    padding:4%;
    padding-top: 20%;
}
.te-card{
    border-radius:35px !important;
    height:60vh;
    padding:10%
}

@media screen and (max-width:600px) {
    .ts-container{
        padding:10%;
        padding-top: 40% ;
    }
    .te-card{
    border-radius:35px !important;
    height:40vh;
    padding:10%;
    margin-bottom: 10%;
}
}
</style>