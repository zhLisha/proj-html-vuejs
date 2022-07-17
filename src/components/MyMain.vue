<template>
  <main>
    <!-- Section 1 Presentation -->
    <SectionOne />

    <!-- Section 2 Faculties Avalaible -->
    <SectionTwo :mainFacultiesArray="facultiesArray" />

    <!-- Section 3 YEar Program -->
    <SectionThree :upComingEvent="eventUpComing" />

  </main>
</template>


<script>
import SectionOne from './Each Section/SectionOne.vue'
import SectionTwo from './Each Section/SectionTwo.vue'
import SectionThree from './Each Section/SectionThree.vue'

export default {
    name: 'MyMain',
    props: {
        facultiesArray: Array,
        eventUpComing: Array
    },

    components: {
        SectionOne,
        SectionTwo, 
        SectionThree,
    }
}
</script>

<style lang="scss" scoped>


</style>