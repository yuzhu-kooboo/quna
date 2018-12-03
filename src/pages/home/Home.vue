<template>
<div>
  <home-header :city="city"></home-header>
  <home-swiper :swiperList="swiperList"></home-swiper>
  <home-recommend :lists="lists"></home-recommend>
  <home-guess :scenicList="scenicList"></home-guess>
  <week-hot :WeekHotLists="WeekHot"></week-hot>
  <where-week :whereWeek="whereWeek"></where-week>
</div>

</template>
<script>
import HomeHeader from './components/HomeHeader'
import HomeSwiper from './components/HomeSwiper'
import HomeRecommend from './components/HomeRecommend'
import HomeGuess from './components/HomeGuess'
import WhereWeek from './components/WhereWeek'
import WeekHot from './components/WeekHot'
import axios from 'axios'

export default {
  name: 'Home',
  data () {
    return {
      city: '武汉',
      lists: [],
      scenicList: [],
      swiperList: [],
      whereWeek: [],
      WeekHot: []
    }
  },
  components: {
    HomeHeader,
    HomeSwiper,
    HomeRecommend,
    HomeGuess,
    WhereWeek,
    WeekHot
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
        this.whereWeek = data.whereWeek
        this.WeekHot = data.WeekHot
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
