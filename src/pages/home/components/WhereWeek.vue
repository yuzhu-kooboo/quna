<template>
  <div class="where">
    <div class="where-week">周末去哪儿</div>
    <week-spot v-for="list of whereWeek" :key="list.id" :list="list"></week-spot>
  </div>
</template>

<script>
import WeekSpot from './WeekSpot'
export default {
  name: 'WhereWeek',
  props: {
    whereWeek: Array,
    required: true
  },
  components: {
    WeekSpot
  }
}
</script>

<style lang="stylus" scoped>
  .where {
    background: #f5f5f5;
    width: 100%
    .where-week{
      height: 0.7rem
      line-height 0.7rem
      margin-left 0.2rem
      color #212121
    }
  }

</style>
