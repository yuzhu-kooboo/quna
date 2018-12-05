<template>
  <div class="city-header">
    <div class="header">
      <router-link to="/"><span class="iconfont">&#xe605;</span></router-link>
      <span>城市选择</span>
    </div>
    <div class="city-search">
      <input type="text" class="search" placeholder="请输入城市名">
    </div>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varible.styl'
  .city-header
    width 100%
    height 1.6rem
    background $bg
    .header
    position relative
      width 100%
      height 0.8rem
      color #fff
      line-height 1rem
      text-align center
      font-size 0.38rem
      .iconfont
        position absolute
        left 0.2rem
        color #fff
    .city-search
      display flex
      justify-content center
      height 0.8rem
      align-items center
      .search
        width 92%
        height 0.6rem
        padding 0 0.12rem
        border-radius 0.1rem
        color #555
</style>
