<template>
  <div class=" sp-container" >

     <div>
         <!-- container for flight and hotel components -->
     </div>
     <div>
         <!-- container for the upcoming specials -->
         <p class="font-2 weight-600 text-center">Special Upcoming Offers</p>   
         <br>

         <v-row no-gutters align="center" justify="center">
             <v-col cols="12" xl="4" lg="4" />
            <v-col cols="12" xl="4" lg="4">
                <div class="pa-2 tab">
                    <specialTabVue @updateValue="updateTab($event)" :tab="tab" :tabs="tabs" />
                </div>
            </v-col>
             <v-col cols="12" xl="4" lg="4" />
         </v-row>
         <br>

        <v-container>
             <v-row v-if="tab==1" no-gutters>
             <v-col   cols="12" v-for="i in specials.team" :key="i[i+1]" xl="4" lg="4">
                 <specialCardVue :info="i"  />
             </v-col>
         </v-row>
         <v-row v-else-if="tab==2" no-gutters>
             <v-col   cols="12" v-for="i in specials.couple" :key="i[i+1]" xl="4" lg="4">
                 <specialCardVue :info="i"  />
             </v-col>
         </v-row>
         <v-row v-else no-gutters>
             <v-col   cols="12" v-for="i in specials.family" :key="i[i+1]" xl="4" lg="4">
                 <specialCardVue :info="i"  />
             </v-col>
         </v-row>
         
        </v-container>
     </div>
  </div>
</template>

<script>
import specialCardVue from './utilities/special.card.vue'
import specialTabVue from './utilities/special.tab.vue'


export default {
    data(){
        return {

            specials:{
                team:[
                    {img:require('../../assets/images/special1.png'),date:"14 FEB 2022",tag:"Relax",title:"Loga Sea",price:700,duration:'3 Days, 3 Nights'},
                    {img:require('../../assets/images/special2.png'),date:"18 JUN 2022",tag:"Adventure",title:"Ansgar Scheffold",price:400,duration:'4 Days, 3 Nights'},
                    {img:require('../../assets/images/special3.png'),date:"22 DEC 2022",tag:"Relax",title:"Lona X",price:340,duration:'7 Days, 6 Nights'},
                ],
                couple:[
                    {img:require('../../assets/images/special1.png'),date:"14 FEB 2022",tag:"Relax",title:"Loga Sea",price:350,duration:'3 Days, 3 Nights'},
                    {img:require('../../assets/images/special2.png'),date:"18 JUN 2022",tag:"Adventure",title:"Ansgar Scheffold",price:200,duration:'4 Days, 3 Nights'},
                    {img:require('../../assets/images/special3.png'),date:"22 DEC 2022",tag:"Relax",title:"Lona X",price:150,duration:'7 Days, 6 Nights'},
                ],
                family:[
                    {img:require('../../assets/images/special1.png'),date:"14 FEB 2022",tag:"Relax",title:"Loga Sea",price:450,duration:'3 Days, 3 Nights'},
                    {img:require('../../assets/images/special2.png'),date:"18 JUN 2022",tag:"Adventure",title:"Ansgar Scheffold",price:350,duration:'4 Days, 3 Nights'},
                    {img:require('../../assets/images/special3.png'),date:"22 DEC 2022",tag:"Relax",title:"Lona X",price:300,duration:'7 Days, 6 Nights'},
                ]
            
            }
            ,
            tab:1,
            tabs:{
                team:1,
                couple:2,
                family:3
            }

        }
    },
    methods:{
        updateTab(value){
            this.tab=value;
        }
    },
    components:{
        specialTabVue,
        specialCardVue
    }

}
</script>

<style>
.sp-container{
    
    padding:4%;
}
.tab{
    margin: 0 10%;
    background:#FFFFFF;
    height: 8vh;
    border-radius: 13px;
}

</style>