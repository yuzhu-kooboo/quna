<template>
  <div class="taglogo">
    <slot></slot>
    <div v-if="time=='today'" class="tag today">今日预定</div>
    <div v-else-if="time=='anytime'" class="tag anytime">随买随用</div>
    <div v-else-if="time=='tomorrow'" class="tag tomorrow">可定明日</div>
  </div>
</template>

<script>
export default {
  name: 'Tag',
  props: ['time']
}
</script>

<style lang="stylus" scoped>
  .taglogo{
    position: relative;
    .tag{
      position: absolute;
      top: 0px;
      left: 0px;
      width: 1.02rem;
      height: 0.38rem;
      border-bottom-right-radius: 0.24rem
      font-size: 0.24rem
      color: #fff;
      line-height: 0.4rem
    }
    .today{
      background: green;
    }
    .anytime{
      background: #FF9C13;
    }
    .tomorrow{
      background: #07CEE7;
    }
  }

</style>
