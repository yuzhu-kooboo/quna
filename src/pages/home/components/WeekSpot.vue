<template>
  <div class="week-spot">
    <img class="week-spot-img" :src="list.urlImg" alt="">
    <div class="text">
      <div class="text-one">{{list.textOne}}</div>
      <div class="text-two">{{list.textTwo}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'WeekSpot',
  props: {
    list: Object,
    required: true
  }
}
</script>

<style lang="stylus">
  .week-spot-img{
    width 100%
  }
  .text{
    padding-left 0.2rem
    padding-top 0.2rem
    background #fff
    .text-one{
      margin-top 0.14rem
    }
    .text-two{
      margin-top 0.2rem
      font-size 0.24rem
      color #616161
      padding-bottom 0.4rem
    }
  }

</style>
