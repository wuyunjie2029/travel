<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-recommend></home-recommend>
    <home-weekend></home-weekend>
  </div>

</template>

<script type="text/ecmascript-6">

  import HomeHeader from './components/header'
  import HomeSwiper from './components/Swiper'
  import HomeIcons from './components/Icons'
  import HomeRecommend from './components/Recommend'
  import HomeWeekend from './components/Weekend'


  export default {
    name: "Home",
    components:{
      HomeHeader:HomeHeader,
      HomeSwiper:HomeSwiper,
      HomeIcons:HomeIcons,
      HomeRecommend:HomeRecommend,
      HomeWeekend:HomeWeekend
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">

</style>
