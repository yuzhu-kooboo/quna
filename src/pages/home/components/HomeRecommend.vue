<template>
  <div class="wrapper">
    <ul class="category">
      <li class="category-item" v-for="list of lists" :key="list.id">
        <a :href="list.aUrl" class="a-category-item">
          <img :src="list.imgUrl" alt="" class="img-category-item">
          <div class="keyword-category-item">{{list.keyWord}}</div>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    lists: Array,
    required: true
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper
    width 100%
    height 3.4rem
    .category
      width 100%
      height 100%
      .category-item
        position relative
        display inline-block
        width 25%
        height 1.6rem
        background #fff
        .a-category-item
          display inline-block
          width 100%
          height 100%
          text-align center
          .img-category-item
            margin-top .2rem
            width 1.1rem
            height 1.1rem
          .keyword-category-item
            position absolute
            bottom 0
            width 100%
            height 0.28rem
            text-align center
</style>
