<template>
  <div class="header">
    <div class="header-back">
      <span class="iconfont">&#xe605;</span>
    </div>
    <div class="header-input"><span class="iconfont">&#xe61e;</span>请输入城市/景点/游玩主题</div>
    <div class="header-city">城市<span class="iconfont">&#xe6aa;</span></div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varible.styl'
  .header
    display: flex
    height: .86rem
    background: $bg
    color: #fff
    line-height: .86rem
    .header-back
      width: .64rem
      float: left
      text-align: center
    .header-input
      flex-grow: 1
      background: #fff
      border-radius: .1rem
      padding-left: .2rem
      margin-top: .12rem
      margin-left: .2rem
      height: .62rem
      line-height: .62rem
      color: #ccc
    .header-city
      width: 1.24rem
      float: right
      text-align: center
</style>
