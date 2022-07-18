<template>
  <main>
    <!-- Section 1 Presentation -->
    <SectionOne />

    <!-- Section 2 Faculties Avalaible -->
    <SectionTwo :mainFacultiesArray="facultiesArray" />

    <!-- Section 3 YEar Program -->
    <SectionThree :upComingEvent="eventUpComing" />

    <!-- Section 4 Latesr Courses + Methods + International Students-->
    <SectionFour :latestCourses="recentCourses" />

    <!-- Section Subscription -->
    <SectionSubscription />

    <!-- Section Partners -->
    <SectionPartners :partnerIcons="partnersArray" />

  </main>
</template>


<script>
// Import Components
import SectionOne from './Each Section/SectionOne.vue'
import SectionTwo from './Each Section/SectionTwo.vue'
import SectionThree from './Each Section/SectionThree.vue'
import SectionFour from './Each Section/SectionFour.vue'
import SectionSubscription from './Each Section/SectionSubscription.vue'
import SectionPartners from './Each Section/SectionPartners.vue'

export default {
    name: 'MyMain',
    props: {
        facultiesArray: Array,
        eventUpComing: Array,
        recentCourses: Array,
        partnersArray: Array
    },

    components: {
        SectionOne,
        SectionTwo, 
        SectionThree,
        SectionFour,
        SectionSubscription,
        SectionPartners,
    }
}
</script>

<style lang="scss" scoped>


</style>