<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>

  </div>

</template>

<script type="text/ecmascript-6">

  import HomeHeader from './components/header'
  import HomeSwiper from './components/Swiper'

  export default {
    name: "Home",
    components:{
      HomeHeader:HomeHeader,
      HomeSwiper:HomeSwiper
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">

</style>
