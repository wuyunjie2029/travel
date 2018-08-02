<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
  </div>

</template>

<script type="text/ecmascript-6">

  import HomeHeader from './components/header'
  import HomeSwiper from './components/Swiper'
  import HomeIcons from './components/Icons'

  export default {
    name: "Home",
    components:{
      HomeHeader:HomeHeader,
      HomeSwiper:HomeSwiper,
      HomeIcons:HomeIcons
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">

</style>
