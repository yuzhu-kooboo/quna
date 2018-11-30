<template>
  <div class="spot">
    <div class="scenic">
      <tag :name="list.tagName"><img slot="today"  class="scenic-img" :src="list.imgUrl" alt=""></tag>
      <div class="scenic-cont">
        <div class="scenic-name">{{list.scenicSpotName}}</div>
        <div class="comment">
          <div class="comment-stars">
            <span v-for="num of list.starsNum" :key="'1'+num" class="iconfont yellow-stars">&#xe676;</span><span v-for="num of (5-list.starsNum)" :key="'2'+num" class="iconfont gray-stars">&#xe676;</span>
          </div>
          <span class="comment-number">{{list.commentNum}}条评论</span>
        </div>
        <div class="price-place">
          <price class="price"><span class="price-number">{{list.price}}</span></price>
          <span class="place">{{list.place}}</span>
        </div>
      </div>
    </div>
    <div v-if="list.showTip" class="tip">{{list.tip}}</div>
  </div>
</template>

<script>
import Price from './Price'
import Tag from './Tag'

export default {
  name: 'ScenicSpot',
  props: {
    list: Object,
    required: true
  },
  components: {
    Price,
    Tag
  }
}
</script>

<style lang="stylus" scoped>
  .spot
    width 100%
    .scenic
      display flex
      .scenic-img
        display flex
        width 2rem
        height 2rem
      .scenic-cont
        margin-left 0.2rem
        height 2rem
        flex-grow 1
        .scenic-name
          width 4rem
          overflow hidden
          white-space nowrap
          text-overflow ellipsis
          color #212121
          margin-top 0.30rem
          font-size 0.32rem
        .comment
          margin-top 0.28rem
          font-size 12px;
          .comment-stars
            display inline-block
            width 1.4rem
            .iconfont
              font-size 12px
            .yellow-stars
              color #ffb436
            .gray-stars
              color #e0e0e0
          .comment-number
            color #616161
        .price-place
          position relative
          margin-top 0.36rem
          .price
            display inline-block
            .price-number
              color #ff8300
              font-size 0.4rem
          .place
            position absolute
            right 0.6rem
            bottom 0.04rem
            font-size 0.24rem
  .tip
    color #f55
    font-size 12px
    margin-top 0.4rem
    margin-left 2.26rem
    margin-bottom 0.2rem
    width 5rem
    overflow hidden
    white-space nowrap
    text-overflow ellipsis
</style>
