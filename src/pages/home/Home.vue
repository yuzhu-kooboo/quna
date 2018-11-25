<template>
<div>
  <home-header></home-header>
  <home-swiper></home-swiper>
  <home-recommend></home-recommend>
</div>

</template>
<script>
import HomeHeader from './components/HomeHeader'
import HomeSwiper from './components/HomeSwiper'
import HomeRecommend from './components/HomeRecommend'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeRecommend
  }
}
</script>

<style>

</style>
