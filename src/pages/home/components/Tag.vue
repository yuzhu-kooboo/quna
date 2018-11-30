<template>
  <div class="taglogo">
    <slot name="today"></slot>
    <slot name="anytime"></slot>
    <slot name="tomorrow"></slot>
    <div v-if="name=='today'" class="tag today">今日预定</div>
    <div v-else-if="name=='anytime'" class="tag anytime">随买随用</div>
    <div v-else-if="name=='tomorrow'" class="tag tomorrow">可定明日</div>
  </div>
</template>

<script>
export default {
  name: 'Tag',
  props: ['name']
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
