<template>
<div id="app">
<router-view/>
<FooterGuide v-show="$route.meta.showFooter"/>
</div>
</template>
<script>
import FooterGuide from './components/FooterGuide/FooterGuide'
export default{
  mounted () { // 异 步 获 取 address
    this.$store.dispatch('getAddress')
  },

  components: {
    FooterGuide
  }
}
</script>
<style lang="stylus" rel="stylesheet/stylus">
.app
  width 100%
  height 100%
  background #f5f5f5
</style>
