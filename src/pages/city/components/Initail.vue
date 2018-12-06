<template>
  <div class="initail">
    <ul>
      <li v-for="(item,index) of letters" :key="index" :ref="item"
       @click="handleInitail"
       @touchstart="handleTouchStart"
       @touchmove="handleTouchMove"
       @touchend="handleTouchEnd">{{item}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Initail',
  props: {
    cities: Object
  },
  data () {
    return {
      startY: 0,
      timer: null
    }
  },
  computed: {
    //数组 = 对象中的属性名
    letters () {
      const letters = []
      for(let i in this.cities) {
        letters.push(i)
      }
      return letters
    }
  },
  methods: {
    handleInitail (e) {
      this.bus.$emit('message', e.target.innerText)
    },
    handleTouchStart (e) {
      console.log("start")
    },
    handleTouchMove (e) {
      if(this.timer) {
        clearTimeout(this.timer)
      }
      this.timer = setTimeout (() => {
        const touchY = e.touches[0].clientY - 80
        const index = Math.floor((touchY - this.startY) / 16)
        if(index >= 0 && index < this.letters.length) {
          this.bus.$emit('message', this.letters[index])
        }
      }, 16)
    },
    handleTouchEnd (e) {
      console.log("end")
    }
  },
  updated () {
    this.startY = this.$refs['A'][0].offsetTop
  }
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
      height 0.32rem
</style>
