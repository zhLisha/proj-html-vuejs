<template>
  <div id="app">
    
    <!-- Header & Jumbotron -->
    <header>
      <MyHeader :navListArray="navList" />
    </header>

    <!-- Main -->
    <MyMain />

    <!-- Footer -->


  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyMain from './components/MyMain.vue'
import NavListJS from '../src/js array/NavListJS.json'

export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain
  },

  data() {
    return {
      navList: NavListJS
    }
  }
}
</script>

<style lang="scss">
@import '@/style/common.scss';
@import '@/style/variables.scss'

</style>
