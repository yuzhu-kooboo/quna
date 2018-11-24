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
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 1500,
        disableOnInteraction: false
      },
      swiperList: [
        {
          id: '001',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1809/12/856f100069809e02.jpg_750x200_e3485a2b.jpg'
        }, {
          id: '002',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1811/ec/f6967f24afeef202.jpg_750x200_9415719f.jpg'
        }, {
          id: '003',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1811/7c/8e5c4ab8ee8b7402.jpg_750x200_dd7a38dd.jpg'
        }
      ]
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
