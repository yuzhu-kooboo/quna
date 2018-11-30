<template>
<div>
  <home-header></home-header>
  <home-swiper></home-swiper>
  <home-recommend></home-recommend>
  <home-guess></home-guess>
</div>

</template>
<script>
import HomeHeader from './components/HomeHeader'
import HomeSwiper from './components/HomeSwiper'
import HomeRecommend from './components/HomeRecommend'
import HomeGuess from './components/HomeGuess'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeRecommend,
    HomeGuess
  }
}
</script>

<style>

</style>
