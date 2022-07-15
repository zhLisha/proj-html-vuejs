<template>
  <div id="app">
    
    <!-- Header & Jumbotron -->
    <MyHeader :navListArray="navList" />

    <!-- Main -->


    <!-- Footer -->


  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import NavListJS from '../src/js array/NavListJS.json'

export default {
  name: 'App',
  components: {
    MyHeader,
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
