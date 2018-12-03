<template>
  <div class="hot">
    <top :top="list.top"><img class="hot-img" :src="list.urlImg" alt=""></top>
    <div class="hot-space_price">
      <div class="hot-space">{{list.space}}</div>
      <price class="hot-price">
        <span class="price-number">{{list.price}}</span>
      </price>
    </div>
  </div>
</template>

<script>
import Price from './Price'
import Top from './Top'

export default {
  name: 'Hot',
  props: ['list'],
  components: {
    Price,
    Top
  }
}
</script>

<style lang="stylus" scoped>
  .hot
    width 2rem
    .hot-img
      width 2rem
      height 2rem
    .hot-space_price
      width 2rem
      height 0.8rem
      text-align center
      .hot-space
        overflow hidden
        text-overflow ellipsis
        color #212121
        margin-top 0.2rem
      .hot-price
        margin-top 0.1rem
        .price-number
          color #ff8300
          font-size 0.4rem
</style>
