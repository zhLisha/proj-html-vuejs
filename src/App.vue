<template>
  <div id="app">
    
    <!-- Header & Jumbotron -->
    <header>
      <MyHeader :navListArray="navList" />
    </header>

    <!-- Main -->
    <MyMain :facultiesArray="facultiesAvalaible" />

    <!-- Footer -->


  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyMain from './components/MyMain.vue'
import NavListJS from '../src/js array/NavListJS.json'
import FacultiesAvalaible from '../src/js array/FacultiesAvalaible.json'

export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain
  },

  data() {
    return {
      navList: NavListJS,
      facultiesAvalaible: FacultiesAvalaible
    }
  }
}
</script>

<style lang="scss">
@import '@/style/common.scss';
@import '@/style/variables.scss'

</style>
