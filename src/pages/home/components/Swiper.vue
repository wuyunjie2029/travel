<template>
  <div class="wrapper">
      <swiper :options="swiperOption">
        <swiper-slide v-for="item of swiperList" :key="item.id">
          <img class="swiper-image" :src="item.imgUrl" alt="">
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>

      </swiper>
  </div>
</template>

<script type="text/ecmascript-6">
  import { swiper, swiperSlide } from 'vue-awesome-swiper'
  export default{
    name: "HomeSwiper",
    data () {
      return {
        swiperOption: {
          pagination: '.swiper-pagination',
          slidesPerView:1,
          autoplay:2000,
          observer:true,
          observeParents:true,
          spaceBetween:30,
          loop:true
        },
        swiperList:[{
          id:"0001",
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1806/3c/c72a1ccd4d7b2202.jpg_750x200_b88bbab4.jpg'
        },{
          id:'0002',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1712/51/36632b2cb850e902.jpg_750x200_fa4120db.jpg'
        },{
          id:'0003',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1807/23/ecfe9185a5f8f702.jpg_750x200_73209fe0.jpg'
        }

        ]
      }

    },
    components: {
      swiper,
      swiperSlide
    },
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
   .wrapper > > >  .swiper-pagination-bullet-active
     background: #fff
   .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 37.5%
    .swiper-image
      width: 100%;

</style>
