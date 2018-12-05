<template>
  <div class="city-list" ref="wrapper">
    <div>
      <div class="present-city">
        <div class="ct">当前城市</div>
        <ul class="present_city">
          <li>厦门</li>
        </ul>
      </div>
      <div class="hot-city">
        <div class="ct">热门城市</div>
        <ul class="hot_cities">
          <li class="hot_city" v-for="list of hotCities" :key="list.id">{{list.name}}</li>
        </ul>
      </div>
      <div class="initial-cities" v-for="(items,key,index) of cities" :key="index">
        <div class="ct" :ref="key">{{key}}</div>
        <ul>
          <li v-for="item of items" :key="item.id">{{item.name}}</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import BScroll from 'better-scroll'
export default {
  name: 'CityList',
  props: {
    cities: Object,
    hotCities: Array
  },
  mounted () {
    this.scroll = new BScroll(this.$refs.wrapper)
    var _this = this
    this.bus.$on('message', res => {
      const dom = _this.$refs[res][0]
      _this.scroll.scrollToElement(dom)
    })
  }
}
</script>

<style lang="stylus" scoped>
  .ct
    padding-left 2%
    height 0.4rem
    line-height 0.4rem
  .city-list
    position absolute
    top 1.6rem
    left 0
    bottom 0
    right  0
    background #dddddd
    width 100%
    overflow hidden
    ul
      display flex
      flex-wrap wrap
      padding-left 2%
      background #fff
      padding-bottom 2%
      li
        width 27%
        border 1px solid #dbdbdd
        line-height 200%
        text-align center
        border-radius 0.06rem
        margin-top 2%
        margin-right 3%
</style>
