<template>
  <div class="initail">
    <ul>
      <li v-for="(item,key,index) of cities" :key="index"
       @click="handleInitail">{{key}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Initail',
  props: {
    cities: Object
  },
  methods: {
    handleInitail (e) {
      this.bus.$emit('message', e.target.innerText)
    }
  },
}
</script>

<style lang="stylus" scoped>
@import '~styles/varible.styl'
  .initail
    display flex
    flex-direction column
    justify-content center
    align-items center
    position: absolute
    top 1.6rem
    bottom 0
    right 0
    width 0.6rem
    li
      color $bg
      font-size 0.3rem
      text-align center
</style>
