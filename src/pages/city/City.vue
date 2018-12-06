<template>
  <div>
    <city-header :cities="cities"></city-header>
    <city-list :cities="cities" :hotCities="hotCities"></city-list>
    <initail :cities="cities"></initail>
  </div>
</template>

<script>
import axios from 'axios'
import CityHeader from './components/CityHeader'
import CityList from './components/CityList'
import Initail from './components/Initail'

export default {
  name: 'City',
  components: {
    CityHeader,
    CityList,
    Initail
  },
  data () {
    return {
      cities: {},
      hotCities: []
    }
  },
  methods: {
    getCityData () {
      axios.get('/static/mock/city.json').then(this.handleCityData)
    },
    handleCityData (res) {
      const data = res.data.data
      console.log(data)
      if (res && data) {
        this.cities = data.cities
        this.hotCities = data.hotCities
      }
    }
  },
  mounted () {
    this.getCityData()
  }
}
</script>

<style>

</style>
