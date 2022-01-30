<template>
  <div style="position:relative;" class=" sp-container" >

  <div class="sh-container">
     
          <v-row no-gutters style="" class="d-flex d-sm-none d-none d-sm-flex d-md-none">
              <v-spacer></v-spacer>
               <div  style="height:100px;width:250px;border-radius:35px;justify-content:center;align-items:center;display:flex"  class="white pa-4 ">
               <div>
                   <v-btn v-if="sw==1" @click="sw=1" large   style="text-transform:none" rounded elevation="0" class="blue mr-1 lighten-5 font-7 weight-600"><v-icon color="blue" size="18">mdi-airplane-takeoff</v-icon>Flight</v-btn>
                   <v-btn v-else large @click="sw=1"  text  style="text-transform:none"  rounded elevation="0" color="black" class=" font-7 weight-600"><v-icon color="blue" size="18">mdi-airplane-takeoff</v-icon>Flight</v-btn>
               </div>
              <div>
                   <v-btn v-if="sw==2" @click="sw=2" large  color="blue lighten-5"  style="text-transform:none" rounded elevation="0" class="font-7 weight-600"><v-icon color="blue" size="18">mdi-home</v-icon>Flight</v-btn>
                   <v-btn v-else @click="sw=2" large text color="black"  style="text-transform:none" rounded elevation="0" class="font-7 weight-600"><v-icon color="blue" size="18">mdi-home</v-icon>Flight</v-btn>
              </div>
           </div>
           <v-spacer></v-spacer>
          </v-row>
     
       <v-container class="hide-xs" >
       
          
            <searchSpecialHomeVue />
      
   </v-container>
  </div>
     <div style="margin-top:20%">
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
import searchSpecialHomeVue from './search.special.home.vue'
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
            },
            sw:1

        }
    },
    methods:{
        updateTab(value){
            this.tab=value;
        }
    },
    components:{
        specialTabVue,
        specialCardVue,
        searchSpecialHomeVue
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
.sh-container{
    position:absolute;
    top:-15%;
    width:100%;
}
@media screen and (max-width:600px) {
    .sh-container{
    position:absolute;
    top:-3em;
    width: 90% !important;
    
} 
.hide-xs{
    display: none !important;
}  
}


</style>