<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont icon-back">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩
    </div>
    <div class="header-right">
      城市
      <span class="iconfont icon-arrow">&#xe64a;</span>
    </div>
  </div>

</template>

<script type="text/ecmascript-6">


  export default {
    name: "HomeHeader"
  }
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
  @import "~styles/varibles.styl"      //@代表src目录

  .header
    display :flex
    line-height: .86rem
    background: $bgColor
    color: #ff
    .header-left
      width: .64rem
      float: left
      .icon-back
        text-align:center
        font-size :.4rem
    .header-input
      flex :1
      height :.64rem
      padding-left :.2rem
      line-height :.64rem
      color :#ccc
      background: #fff
      margin-left: .2rem
      margin-top: .12rem
      border-radius :.1rem
    .header-right
      width :1.24rem
      float :right
      text-align :center
      .icon-arrow
        margin-left :-.04rem
        font-size :.24rem
</style>
