<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}
          </p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>

</template>

<script type="text/ecmascript-6">
  export default {
    name:'HomeWeekend',
    data () {
      return {
        recommendList:[{
          id:'0001',
          imgUrl:'http://img1.qunarzz.com/sight/source/1505/4e/3e87ee62e59cdb.jpg_r_640x214_fe6cc902.jpg',
          desc:'浪漫的云漫温泉',
          title:'杭州云漫温泉'
        },{
          id:'0002',
          imgUrl:'http://img1.qunarzz.com/sight/source/1505/4e/3e87ee62e59cdb.jpg_r_640x214_fe6cc902.jpg',
          desc:'浪漫的云漫温泉',
          title:'杭州云漫温泉'
        },{
          id:'0003',
          imgUrl:'http://img1.qunarzz.com/sight/source/1505/4e/3e87ee62e59cdb.jpg_r_640x214_fe6cc902.jpg',
          desc:'浪漫的云漫温泉',
          title:'杭州云漫温泉'
        },]
      }
    }
  }
</script>

<style lang="stylus" scoped rel="stylesheet/stylus">
  @import "~styles/mixins.styl"

    .recommend-title
      background: #eee
      /*text-index :.2rem*/
      padding-left:.2rem;
      margin-top:.2rem;
      line-height:.8rem
    .item-img-wrapper
      height :0
      overflow :hidden
      padding-bottom :33.9%
      .item-img
        width :100%
    .item-info
      padding :.1rem
      flex :1
      min-width :0   //让多余的内容显示...
      .item-title
        line-height :.54rem
        font-size:.32rem
        ellipsis()
      .item-desc
        line-height:.4rem
        color :#ccc
        ellipsis()

</style>
