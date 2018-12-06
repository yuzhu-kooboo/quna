<template>
  <div class="city-header">
    <div class="header">
      <router-link to="/">
        <span class="iconfont">&#xe605;</span>
      </router-link>
      <span>城市选择</span>
    </div>
    <search-city :cities="cities"></search-city>
  </div>
</template>

<script>
import SearchCity from "./SearchCity";
export default {
  name: "CityHeader",
  props: {
    cities: {
      type: Object,
      required: true
    }
  },
  components: {
    SearchCity
  }
};
</script>

<style lang="stylus" scoped>
@import '~styles/varible.styl';

.city-header {
  width: 100%;
  height: 1.6rem;
  background: $bg;

  .header, position relative {
    width: 100%;
    height: 0.8rem;
    color: #fff;
    line-height: 1rem;
    text-align: center;
    font-size: 0.38rem;

    .iconfont {
      position: absolute;
      left: 0.2rem;
      color: #fff;
    }
  }
}
</style>
