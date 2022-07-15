<template>
  <main>
    <!-- Section 1 -->
    <SectionOne />

    <!-- Section 2 -->
    <SectionTwo :mainFacultiesArray="facultiesArray" />

  </main>
</template>


<script>
import SectionOne from './Each Section/SectionOne.vue'
import SectionTwo from './Each Section/SectionTwo.vue'

export default {
    name: 'MyMain',
    props: {
        facultiesArray: Array
    },

    components: {
        SectionOne,
        SectionTwo, 
    }
}
</script>

<style lang="scss" scoped>


</style>