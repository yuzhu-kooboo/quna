<template>
<div>
  <home-header :city="city"></home-header>
  <home-swiper :swiperList="swiperList"></home-swiper>
  <home-recommend :lists="lists"></home-recommend>
  <home-guess :scenicList="scenicList"></home-guess>
</div>

</template>
<script>
import HomeHeader from './components/HomeHeader'
import HomeSwiper from './components/HomeSwiper'
import HomeRecommend from './components/HomeRecommend'
import HomeGuess from './components/HomeGuess'
import axios from 'axios'

export default {
  name: 'Home',
  data () {
    return {
      city: '武汉',
      lists: [],
      scenicList: [],
      swiperList: []
    }
  },
  components: {
    HomeHeader,
    HomeSwiper,
    HomeRecommend,
    HomeGuess
  },
  methods: {
    getHomeData () {
      axios.get('/static/mock/home.json').then(this.getHomeDataSucess)
    },
    getHomeDataSucess (res) {
      const data = res.data.data
      if (res.data.ret === true && data.city) {
        this.city = data.city
        this.lists = data.lists
        this.scenicList = data.scenicList
        this.swiperList = data.swiperList
      }
    }
  },
  mounted () {
    this.getHomeData()
  }
}
</script>

<style>

</style>
