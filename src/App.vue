<template>
  <div id="app">
    <router-view />
    <FooterGuide v-show="$route.meta.showFooter "/>
  </div>
</template>

<script>
import FooterGuide from './components/FooterGuide/FooterGuide'
// import {reqCategorys} from './api'
import {mapActions} from 'vuex'
export default {
  name: 'App',
  components: {
    FooterGuide
  },
  mounted () {
    // 异步获取 address
    // this.$store.dispatch('getAddress')
    this.getAddress()
  },
  methods: {
    ...mapActions(['getAddress'])
  }

  // async mounted () {
  //   console.log(1)
  //   const result = await reqCategorys()
  //   console.log(result)
  // }
}
</script>

<style lang="stylus" rel="stylesheet/stylus">
//#app {
//  font-family: 'Avenir', Helvetica, Arial, sans-serif;
//  -webkit-font-smoothing: antialiased;
//  -moz-osx-font-smoothing: grayscale;
//  text-align: center;
//  color: #2c3e50;
//  margin-top: 60px;
//}
</style>
