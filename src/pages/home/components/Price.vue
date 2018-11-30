<template>
  <div>
    <span class="theprice">￥</span><slot></slot><span class="price-rise">起</span>
  </div>
</template>

<script>
export default {
  name: 'Price'
}
</script>

<style lang="stylus">
  .theprice
    color red
  .price-rise
    color #616161
</style>
