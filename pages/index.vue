<template>
  <div class="home">
    <app-home-intro></app-home-intro>
    <app-home-services></app-home-services>
    <app-home-numbers></app-home-numbers>
    <app-home-why></app-home-why>
    <app-home-consult></app-home-consult>
    <app-home-team></app-home-team>
    <app-home-contact></app-home-contact>
  </div>
</template>

<script>
import AppHomeConsult from '../components/home/AppHomeConsult.vue'
import AppHomeContact from '../components/home/AppHomeContact.vue'
import AppHomeIntro from '../components/home/AppHomeIntro.vue'
import AppHomeNumbers from '../components/home/AppHomeNumbers.vue'
import AppHomeServices from '../components/home/AppHomeServices.vue'
import AppHomeTeam from '../components/home/AppHomeTeam.vue'
import AppHomeWhy from '../components/home/AppHomeWhy.vue'



export default {
  name: 'Home',
  components: {
    AppHomeIntro,
    AppHomeServices,
    AppHomeNumbers,
    AppHomeWhy,
    AppHomeConsult,
    AppHomeTeam,
    AppHomeContact
    
  }
}
</script>
