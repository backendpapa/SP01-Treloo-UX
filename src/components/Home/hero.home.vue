<template>
  <div>
   <v-row align="center" justify="center" class="hero" no-gutters>
       <v-col cols="12" xl="2" lg="2" />
       <v-col cols="12" xl="8" lg="8">
         <v-container>
            <p class="font-1  font-title white--text">Discover Your Life, Travel Where You Want</p>
          <p class="font-4 font-desc  white--text">Would you explore natur paradise in the world, let’s find the best destination in world with us.</p>
         </v-container>
       </v-col>
       <v-col cols="12" xl="2" lg="2" />

    </v-row>
  </div>
</template>

<script>
  

  export default {
    name: 'Hero',

    components: {
      
    },
  }
</script>
<style>
.hero{
  height :140vh;
  background: url('../../assets/images/hero.png');
  background-size: cover;
}
.font-title{
  font-weight: 600;
  text-align: center;
}
.font-desc{
  font-weight: 500;
  text-align: center;
}

@media screen and (max-width:600px) {
  .hero{
  height :120vh;
  background: url('../../assets/images/hero.png');
  background-size: cover;
  padding: 5%;
}
    .font-title{
      text-align: left;
      line-height: 1.2;
    }

    .font-desc{
        font-weight: 500;
        text-align: left;
    }
}
</style>
