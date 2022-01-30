<template>
  <div class="recommend-container">
      <p class="font-2 weight-600 text-center">Recommended Destination</p>
      <br>

       <v-row no-gutters align="center" justify="center">
             <v-col cols="12" xl="4" lg="4" />
            <v-col cols="12" xl="4" lg="4">
                <div class="pa-2 tab2">
                    <recommendTabVue @updateValue="updateTab($event)" :tab="tab" :tabs="tabs" />
                </div>
            </v-col>
             <v-col cols="12" xl="4" lg="4" />
         </v-row>

         <br>
        <v-row >
            <v-col v-for="i in recommends" :key="i" cols="12" xl="3" lg="3">
                 <recommendCardVue :img="i" />
            </v-col>
        </v-row>
      
  </div>
</template>

<script>
import recommendCardVue from './utilities/recommend.card.vue'
import recommendTabVue from './utilities/recommend.tab.vue'


export default {
    components:{
        recommendTabVue,
        recommendCardVue
    },
    data(){
        return {
             tab:1,
            tabs:{
                team:1,
                couple:2,
                family:3
            },
            recommends:[
                {img:require('../../assets/images/dest1.png'),rating:3.4},
                {img:require('../../assets/images/dest2.png'),rating:4.5},
                {img:require('../../assets/images/dest3.png'),rating:4.2},
                {img:require('../../assets/images/dest4.png'),rating:4.2},
            ]
        }
    }
}
</script>

<style>
.recommend-container{
    padding:4%;
}
.tab2{
    margin: 0 8%;
    
    height: 8vh;
    border-radius: 13px;
}
@media screen and (max-width:600px) {
    .recommend-container{
    padding:12%;
}
}
</style>