<template>
  <div>
    <v-card class="pa-2 card" color="white" flat>
      <div class="card-inner-1">
        <v-row style="height: 100%" class="pa-4" no-gutters>
          <v-col cols="10" class="">
            <v-img eager :src="info.img"> </v-img>
          </v-col>
          <v-col cols="2">
            <p class="special-text ml-5 font-6 mt-5">{{info.date}}</p>
          </v-col>
        </v-row>
      </div>

      <div class="card-inner-2">
        <v-row align="center" justify="center" no-gutters>
          <v-chip color="red chip lighten-5" class="pl-3 pr-3" small
            ><span class="font-7 red--text">{{info.tag}}</span></v-chip
          >
          <p class="mb-n1 ml-3 font-7 grey--text">{{info.duration}}</p>
          <v-spacer></v-spacer>
        </v-row>
       
       <div class="mt-2">
            <p class="font-4 weight-600">{{info.title}}</p>
            <v-row no-gutters align="center" justify="center">
                <p class="font-4 weight-500 mb-n1">{{info.price}}$<span class="font-6 grey--text">/Person</span></p>
                <v-spacer></v-spacer>
                <v-btn   elevation="0" style="text-transform:none" class="font-7 d-none d-sm-flex blue--text" color="blue lighten-5">Book Now</v-btn>
                <v-btn small   elevation="0" style="text-transform:none" class="font-7 d-flex d-sm-none" color="blue lighten-5 blue--text">Book Now</v-btn>
            </v-row>
       </div>
      </div>
    </v-card>
  </div>
</template>

<script>
export default {
    props:['info']
};
</script>

<style>
.card {
  height: 70vh;
  border-radius: 45px !important;

  margin: 5%;
}
.card-inner-1 {
  height: 65%;
}
.card-inner-2 {
  height: 35%;
  padding: 3% 6%;
}
.special-text {
  writing-mode: vertical-rl;
  letter-spacing: 7px;
}
@media screen and (max-width: 600px) {
  .card {
    height: 50vh;
    border-radius: 45px !important;

    margin: 5%;
  }
  .chip {
    height: 18px !important;
  }
  .card-inner-2 {
  height: 35%;
  padding: 2% 6%;
}
}
</style>