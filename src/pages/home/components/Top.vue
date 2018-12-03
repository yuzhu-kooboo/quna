<template>
  <div class="toplogo">
    <slot></slot>
    <div v-if="top=='topone'" class="top topone">Top.1</div>
    <div v-else-if="top=='toptwo'" class="top toptwo">Top.2</div>
    <div v-else-if="top=='topthree'" class="top topthree">Top.3</div>
  </div>
</template>

<script>
export default {
  name: 'Top',
  props: ['top']
}
</script>

<style lang="stylus" scoped>
.toplogo
  position relative
  .top
    position absolute
    left 0
    top 0
    width 0.8rem
    height 0.3rem
    color #fff
    border-radius 0.04rem
    background-color: #FF282D
  .toptwo
    background-color: #FF6C1D
  .topthree
    background-color: #FFAA1E
</style>
