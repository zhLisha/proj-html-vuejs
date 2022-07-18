<template>
  <div id="app">
  
    <!-- Header & Jumbotron -->
    <header>
      <MyHeader :navListArray="navList" />
    </header>

    <!-- Main -->
    <MyMain :facultiesArray="facultiesAvalaible" :eventUpComing="futureEvents" :recentCourses="latestCourses" :partnersArray="partnersIcon" />

    <!-- Footer -->
    <SectionFooter :eduPrimeArray="eduPrime" :networkingArray="netwotking" :facilityArray="facilitySearch" />

  </div>
</template>

<script>
// Import Components
import MyHeader from './components/MyHeader.vue'
import MyMain from './components/MyMain.vue'
import SectionFooter from './components/Each Section/SectionFooter.vue'

// Import Json Package
// Header
import NavListJS from '../src/js array/NavListJS.json'
// Main
import FacultiesAvalaible from '../src/js array/FacultiesAvalaible.json'
import EventsDetails from '../src/js array/EventsDetails.json'
import LatestCourses from '../src/js array/LatestCourses.json'
import PartnersIcons from '../src/js array/PartnersIcons'
// Footer
import GetEduPrimeFooter from '../src/js array/GetEduPrimeFooter'
import NetworkingFooter from '../src/js array/NetworkingFooter'
import SearchFacilityFooter from '../src/js array/SearchFacilityFooter'


export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain,
    SectionFooter
  },

  data() {
    return {
      // Header
      navList: NavListJS,
      // Main
      facultiesAvalaible: FacultiesAvalaible,
      futureEvents: EventsDetails,
      latestCourses: LatestCourses,
      partnersIcon: PartnersIcons,
      // Footer
      eduPrime: GetEduPrimeFooter,
      netwotking: NetworkingFooter,
      facilitySearch: SearchFacilityFooter
    }
  }
}
</script>

<style lang="scss">
@import '@/style/common.scss';
@import '@/style/variables.scss'

</style>
