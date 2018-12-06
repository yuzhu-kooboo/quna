<template>
  <div>
    <div class="city-search">
      <input v-model="keyword" type="text" class="search" placeholder="请输入城市名">
    </div>
    <div class="search_city" ref="search_city"  v-show="keyword">
      <ul>
        <li class="city border-bottom" v-for="list of lists" :key="list.id">{{list.name}}</li>
        <li class="city border-bottom" v-show="hasCity">未找到您搜索的城市~_~</li>
      </ul>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'

export default {
  name: "SearchCity",
  props: {
    cities: Object
  },
  data () {
    return {
      keyword: '',
      lists: [],
      timer: null
    }
  },
  watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      if (!this.keyword) {
        this.lists = []
        return
      }
      this.timer = setTimeout(() => {
        const result = []
        for (let i in this.cities) {
          this.cities[i].forEach((value) => {
            if (value.spell.indexOf(this.keyword) > -1 || value.name.indexOf(this.keyword) > -1) {
              result.push(value)
            }
          })
        }
        this.lists = result
      }, 200)
      
    }
  },
  computed: {
    hasCity () {
      return !this.lists.length
    }
  },
  mounted () {
    this.scroll = new Bscroll(this.$refs.search_city)
  }
};
</script>

<style lang="stylus" scoped>
.city-search {
  display: flex;
  justify-content: center;
  height: 0.8rem;
  align-items: center;

  .search {
    width: 92%;
    height: 0.6rem;
    padding: 0 0.12rem;
    border-radius: 0.1rem;
    color: #555;
    text-align: center
  }
}

.search_city {
  z-index: 1;
  position: absolute;
  overflow hidden
  top: 1.6rem;
  width: 100%;
  background: #fff;
  bottom: 0;
  right: 0;
  left: 0;
  .city{
    line-height: 0.6rem;
    padding-left: 0.2rem;
    color: #666;
  }
}
</style>
