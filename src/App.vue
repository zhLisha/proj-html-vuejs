<template>
  <div id="app">
    
    <!-- Header & Jumbotron -->
    <header>
      <MyHeader :navListArray="navList" />
    </header>

    <!-- Main -->
    <MyMain :facultiesArray="facultiesAvalaible" :eventUpComing="futureEvents" :recentCourses="latestCourses" :partnersArray="partnersIcon" />

    <!-- Footer -->


  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyMain from './components/MyMain.vue'
import NavListJS from '../src/js array/NavListJS.json'
import FacultiesAvalaible from '../src/js array/FacultiesAvalaible.json'
import EventsDetails from '../src/js array/EventsDetails.json'
import LatestCourses from '../src/js array/LatestCourses.json'
import PartnersIcons from '../src/js array/PartnersIcons'

export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain
  },

  data() {
    return {
      navList: NavListJS,
      facultiesAvalaible: FacultiesAvalaible,
      futureEvents: EventsDetails,
      latestCourses: LatestCourses,
      partnersIcon: PartnersIcons
    }
  }
}
</script>

<style lang="scss">
@import '@/style/common.scss';
@import '@/style/variables.scss'

</style>
