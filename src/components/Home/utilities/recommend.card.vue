<template>
  <div>
      <v-card hover class=" white card-rc">
          <div class="rc-inner-1">
             
              <v-img :src="img.img"></v-img>
              <div class="chip-container">
                 <v-row no-gutters>
                     <v-spacer></v-spacer>
                     <v-chip color="white" class="weight-600" x-small    ><v-rating class="ml-n2" color="yellow darken-1" length="1" x-small dense value="5" v-model="rating"></v-rating> {{img.rating}}</v-chip>
                 </v-row>
             </div>
          </div>
          <div class="rc-inner-2">
              <p class="mb-n1 font-5 weight-600">Kina Mountain</p>
              <p class="mb-n1 mt-2 font-7 grey--text weight-600"><v-icon color="red"  class="mt-n1" size="15">mdi-map-marker</v-icon> Cambodia</p>
          </div>
      </v-card>
  </div>
</template>

<script>
export default {
data(){
    return {
        rating:1
    }
},
props:['img']
}
</script>

<style>
.card-rc{
    height: 40vh;
    border-radius: 35px !important;
}
.rc-inner-1{
    height: 70%;
    padding:4%;
}
.rc-inner-2{
    padding:4%;
    height: 30%;
}
.chip-container{
    position: absolute;
    top:10%;
    right:10%;
}

@media screen  and (max-width:600px) {
    .card-rc{
    height: 40vh;
    border-radius: 35px !important;

}
.rc-inner-2{
    padding:10% 5%;
    height: 30%;
}

}
</style>