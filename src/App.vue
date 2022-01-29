<template>
  <v-app>
    <!-- <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar> -->

    <v-main>
      <router-view/>
    </v-main>
    <v-footer class="bg-1 ">
     <v-container>
        <v-row no-gutters style="" class="footer d-none d-sm-flex">
            <p class="font-7">© 2022 Treloo LLC - All right reserved.</p>
            <v-spacer></v-spacer>
            <div style="display:flex">
                <v-btn style="flex:1;text-transform:none" class="font-7 mr-2" x-small text plain>Review</v-btn>
                <v-btn style="flex:1;text-transform:none" class="font-7 mr-2" x-small text plain>Tips</v-btn>
                <v-btn style="flex:1;text-transform:none" class="font-7 mr-2" x-small text plain>Alerts</v-btn>
                <v-btn style="flex:1;text-transform:none" class="font-7 mr-2" x-small text plain>Blog</v-btn>
            </div>
      </v-row>
       <v-row no-gutters style="width:100%" class="footer d-flex d-sm-none">
           
            <v-spacer></v-spacer>
            <div>
              <div style="display:flex">
                <v-btn style="flex:1;text-transform:none" class="font-7 mr-2" x-small text plain>Review</v-btn>
                <v-btn style="flex:1;text-transform:none" class="font-7 mr-2" x-small text plain>Tips</v-btn>
                <v-btn style="flex:1;text-transform:none" class="font-7 mr-2" x-small text plain>Alerts</v-btn>
                <v-btn style="flex:1;text-transform:none" class="font-7 mr-2" x-small text plain>Blog</v-btn>
            </div>
             <p class="font-7 text-center">© 2022 Treloo LLC - All right reserved.</p>
            </div>
            <v-spacer></v-spacer>
      </v-row>
     </v-container>
    </v-footer>
  </v-app>
</template>

<script>
import "./css/fonts.css"
export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
<style>
.footer{
  padding:4%;
}
@media screen and (max-width:500px) {
 .footer{
  padding:10%;
}   
}
</style>
