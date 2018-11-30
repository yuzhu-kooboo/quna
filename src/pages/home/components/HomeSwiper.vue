<template>
  <div class="home-header-swiper">
    <swiper :options="swiperOption">
    <swiper-slide v-for="list of swiperList" :key="list.id"><img class="swiper-img" :src="list.imgUrl" alt=""></swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    swiperList: Array,
    required: true
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 1500,
        disableOnInteraction: false
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
  .home-header-swiper >>> .swiper-pagination-bullet-active
    background #fff!important
  .home-header-swiper
    width 100%
    height 0
    padding-bottom 26.7%
    overflow hidden
    .swiper-img
      width: 100%
</style>
