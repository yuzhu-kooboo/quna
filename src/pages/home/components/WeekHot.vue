<template>
  <div class="box">
    <div class="week-hot">
      <div class="week-hot-title">
        <img class="week-hot-img" src="http://img1.qunarzz.com/piao/fusion/1711/16/bfbb9874e8f11402.png" alt="">
        <span>本周热门榜单</span>
      </div>
      <router-link to="">
        <div class="week-all-hot">
          <span>全部榜单</span>
          <span class="iconfont">></span>
        </div>
      </router-link>
    </div>
    <div class="hotlist">
      <hot class="hotscenicspot" v-for="list of WeekHotLists" :key="list.id" :list="list"></hot>
    </div>
  </div>
</template>
<script>
import Hot from './Hot'
export default {
  name: 'WeekHot',
  props: {
    WeekHotLists: Array,
    required: true
  },
  components: {
    Hot
  }
}
</script>

<style lang="stylus" scoped>
.box
  .week-hot
    position: relative
    margin-top 0.4rem
    widht 100%
    height 0.4rem
    .week-hot-title
      display inline-block
      .week-hot-img
        width 0.32rem
        height 0.32rem
        margin-top -0.08rem
    .week-all-hot
      position absolute
      right 0.4rem
      top 0rem
      color #616161
  .hotlist
    white-space nowrap
    overflow-x auto
    margin-top 0.2rem
    margin-bottom 0.2rem
    .hotscenicspot
      display inline-block
      margin-left 0.2rem
</style>
