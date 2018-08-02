<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page,index) of pages" :key="page.index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-imgcontent" :src="item.imgUrl" alt=""/>
          </div>

          <p class="keywords">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script type="text/ecmascript-6">
  export default{
    name: 'HomeIcons',
    data () {
      return {
        iconList:[{
          id:'0001',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc:'景点门票'
        },{
          id:'0002',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
          desc:'一日游'
        },{
          id:'0003',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
          desc:'杭州必游'
        },{
          id:'0004',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/75/eca3ce656c886502.png',
          desc:'漂流'
        },{
          id:'0005',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/6a/45f595250c73d102.png',
          desc:'夏日玩水'
        },{
          id:'0006',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/17/99402a22ce4af302.png',
          desc:'西湖'
        },{
          id:'0007',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/e3/67df61427c8e1302.png',
          desc:'宋城千古情'
        },{
          id:'0008',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/95/8d02011d149bdb02.png',
          desc:'汽车票'
        },{
          id:'0008',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/95/8d02011d149bdb02.png',
          desc:'汽车票'
        }]
      }
    },
    computed:{
      pages () {
        const pages = [];
        this.iconList.forEach((item,index)=> {
          const page = Math.floor(index / 8);
           if(!pages[page]){
             pages[page] = []
           }
           pages[page].push(item)

        })
        return pages
      }
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'

  . icons >>>  .swiper-container
    width: 100%
    height: 0
    padding-bottom: 50%

  .icon
    position: relative
    overflow: hidden
    width: 25%
    height: 0
    padding-bottom: 25%
    float: left
    .icon-img
      position: absolute
      left: 0
      top: 0
      right: 0
      bottom: .44rem
      .icon-imgcontent
        display block
        padding-top: .2rem
        margin: 0 auto
        width: 1.29rem
    .keywords
      position: absolute
      left: 0
      right: 0
      bottom: 0
      height: .44rem
      line-height: .44rem
      text-align: center
      color: $darkTextColor
      ellipsis()
</style>
