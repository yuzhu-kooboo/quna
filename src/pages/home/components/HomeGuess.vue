<template>
<div class="guess">
  <div class="youlove">
    <img class="love" :src="loveUrl" alt="">
    <span>猜你喜欢</span>
  </div>
  <scenic-spot v-for="list of scenicList" :key="list.id" :list='list' class="scenic_spot"></scenic-spot>
</div>
</template>

<script>
import ScenicSpot from './ScenicSpot'
export default {
  name: 'HomeGuess',
  props: {
    scenicList: Array,
    required: true
  },
  components: {
    ScenicSpot
  },
  data () {
    return {
      loveUrl: 'http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png'
    }
  }
}
</script>

<style lang="stylus" scoped>
  .youlove
    width 100%
    height 0.8rem
    line-height 0.8rem
    margin-left 0.16rem
    .love
      width 0.32rem
      height 0.32rem
      margin-top -0.08rem
  .scenic_spot
    margin-left 0.2rem
    margin-top 0.2rem
    padding-bottom 0.2rem
    border-bottom 1px solid #dbdbdb
</style>
