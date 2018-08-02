<template>
  <div>
    <div class="recommend-title">猜你喜欢</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">

        <img class="item-img" :src="item.imgUrl" alt="">

        <div class="item-info">
          <p class="item-title">{{item.title}}
          </p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button" >查看详情</button>
        </div>
      </li>
    </ul>
  </div>

</template>

<script type="text/ecmascript-6">
  export default {
    name:'HomeRecommend',
    data () {
      return {
        recommendList:[{
          id:'0001',
          imgUrl:'http://img1.qunarzz.com/sight/p0/201408/14/dba7220ac844600c07a1af703f640935.jpg_200x200_a84b7d79.jpg',
          desc:'浪漫的云漫温泉',
          title:'杭州云漫温泉'
        },{
          id:'0002',
          imgUrl:'http://img1.qunarzz.com/sight/p0/201401/06/3fbbddda915cb7637439d484440d36be.jpg_200x200_a54e87dd.jpg',
          desc:'浪漫的云漫温泉',
          title:'杭州云漫温泉'
        },{
          id:'0003',
          imgUrl:'http://img1.qunarzz.com/sight/p0/201406/23/6a12f3746bdb338390706f3d7ac34f87.jpg_200x200_86db3cde.jpg',
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
.item
  overflow :hidden
  display :flex
  height :1.9rem

  .item-img
    height :1.7rem
    width :1.7rem
    padding :.1rem
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
    .item-button
      line-height:.44rem
      margin-top:.16rem
      background: #ff9300
      padding :0 .2rem
      border-radius :.06rem
      color :#fff
</style>
