<template>
  <div>
   <heroHomeVue />
  <div class="bg-1">
     <specialsHomeVue />
    <v-container>
       <contactHomeVue />
       <recommendHomeVue />
       <testimonialHomeVue />
       <discountHomeVue />
    </v-container>
  </div>
  </div>
</template>

<script>
import contactHomeVue from '../components/Home/contact.home.vue'
import discountHomeVue from '../components/Home/discount.home.vue'
import heroHomeVue from '../components/Home/hero.home.vue'
import recommendHomeVue from '../components/Home/recommend.home.vue'
import specialsHomeVue from '../components/Home/specials.home.vue'
import testimonialHomeVue from '../components/Home/testimonial.home.vue'



  export default {
    name: 'Home',

    components: {
      heroHomeVue,
      specialsHomeVue,
      contactHomeVue,
      recommendHomeVue,
      testimonialHomeVue,
      discountHomeVue
    },
  }
</script>
<style>

</style>
