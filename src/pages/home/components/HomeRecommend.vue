<template>
  <div class="wrapper">
    <ul class="category">
      <li class="category-item" v-for="list of lists" :key="list.id">
        <a :href="list.aUrl" class="a-category-item">
          <img :src="list.imgUrl" alt="" class="img-category-item">
          <div class="keyword-category-item">{{list.keyWord}}</div>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      lists: [
        {
          id: '001',
          aUrl: 'https://touch.piao.qunar.com/touch/list_%E5%8E%A6%E9%97%A8_%E6%99%AF%E7%82%B9%E9%97%A8%E7%A5%A8.html?region=%E5%8E%A6%E9%97%A8&cat=from_area%253Dts_type_nav%2526from_index%253D0%2526from_value%253D%2525E6%252599%2525AF%2525E7%252582%2525B9%2525E9%252597%2525A8%2525E7%2525A5%2525A8%2526dist_city%253D%2525E5%25258E%2525A6%2525E9%252597%2525A8&isForeign=false&pageSize=10',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          keyWord: '景点门票'
        }, {
          id: '002',
          aUrl: 'https://touch.piao.qunar.com/touch/list_%E5%8E%A6%E9%97%A8_%E6%99%AF%E7%82%B9%E9%97%A8%E7%A5%A8.html?region=%E5%8E%A6%E9%97%A8&cat=from_area%253Dts_type_nav%2526from_index%253D0%2526from_value%253D%2525E6%252599%2525AF%2525E7%252582%2525B9%2525E9%252597%2525A8%2525E7%2525A5%2525A8%2526dist_city%253D%2525E5%25258E%2525A6%2525E9%252597%2525A8&isForeign=false&pageSize=10',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
          keyWord: '一日游'
        }, {
          id: '003',
          aUrl: 'https://touch.piao.qunar.com/touch/list_%E5%8E%A6%E9%97%A8_%E6%99%AF%E7%82%B9%E9%97%A8%E7%A5%A8.html?region=%E5%8E%A6%E9%97%A8&cat=from_area%253Dts_type_nav%2526from_index%253D0%2526from_value%253D%2525E6%252599%2525AF%2525E7%252582%2525B9%2525E9%252597%2525A8%2525E7%2525A5%2525A8%2526dist_city%253D%2525E5%25258E%2525A6%2525E9%252597%2525A8&isForeign=false&pageSize=10',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
          keyWord: '厦门必游'
        }, {
          id: '004',
          aUrl: 'https://touch.piao.qunar.com/touch/list_%E5%8E%A6%E9%97%A8_%E6%99%AF%E7%82%B9%E9%97%A8%E7%A5%A8.html?region=%E5%8E%A6%E9%97%A8&cat=from_area%253Dts_type_nav%2526from_index%253D0%2526from_value%253D%2525E6%252599%2525AF%2525E7%252582%2525B9%2525E9%252597%2525A8%2525E7%2525A5%2525A8%2526dist_city%253D%2525E5%25258E%2525A6%2525E9%252597%2525A8&isForeign=false&pageSize=10',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/97/02f5043b51b2102.png',
          keyWord: '鼓浪屿'
        }, {
          id: '005',
          aUrl: 'https://touch.piao.qunar.com/touch/list_%E5%8E%A6%E9%97%A8_%E6%99%AF%E7%82%B9%E9%97%A8%E7%A5%A8.html?region=%E5%8E%A6%E9%97%A8&cat=from_area%253Dts_type_nav%2526from_index%253D0%2526from_value%253D%2525E6%252599%2525AF%2525E7%252582%2525B9%2525E9%252597%2525A8%2525E7%2525A5%2525A8%2526dist_city%253D%2525E5%25258E%2525A6%2525E9%252597%2525A8&isForeign=false&pageSize=10',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/96/c70f1e85ae4a4f02.png',
          keyWord: '自然风光'
        }, {
          id: '006',
          aUrl: 'https://touch.piao.qunar.com/touch/list_%E5%8E%A6%E9%97%A8_%E6%99%AF%E7%82%B9%E9%97%A8%E7%A5%A8.html?region=%E5%8E%A6%E9%97%A8&cat=from_area%253Dts_type_nav%2526from_index%253D0%2526from_value%253D%2525E6%252599%2525AF%2525E7%252582%2525B9%2525E9%252597%2525A8%2525E7%2525A5%2525A8%2526dist_city%253D%2525E5%25258E%2525A6%2525E9%252597%2525A8&isForeign=false&pageSize=10',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png',
          keyWord: '游乐场'
        }, {
          id: '007',
          aUrl: 'https://touch.piao.qunar.com/touch/list_%E5%8E%A6%E9%97%A8_%E6%99%AF%E7%82%B9%E9%97%A8%E7%A5%A8.html?region=%E5%8E%A6%E9%97%A8&cat=from_area%253Dts_type_nav%2526from_index%253D0%2526from_value%253D%2525E6%252599%2525AF%2525E7%252582%2525B9%2525E9%252597%2525A8%2525E7%2525A5%2525A8%2526dist_city%253D%2525E5%25258E%2525A6%2525E9%252597%2525A8&isForeign=false&pageSize=10',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/89/55083b0f1951f302.png',
          keyWord: '两江夜游'
        }, {
          id: '008',
          aUrl: 'https://touch.piao.qunar.com/touch/list_%E5%8E%A6%E9%97%A8_%E6%99%AF%E7%82%B9%E9%97%A8%E7%A5%A8.html?region=%E5%8E%A6%E9%97%A8&cat=from_area%253Dts_type_nav%2526from_index%253D0%2526from_value%253D%2525E6%252599%2525AF%2525E7%252582%2525B9%2525E9%252597%2525A8%2525E7%2525A5%2525A8%2526dist_city%253D%2525E5%25258E%2525A6%2525E9%252597%2525A8&isForeign=false&pageSize=10',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
          keyWord: '打卡圣地'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper
    width 100%
    height 3.4rem
    .category
      width 100%
      height 100%
      .category-item
        position relative
        display inline-block
        width 25%
        height 1.6rem
        background #fff
        .a-category-item
          display inline-block
          width 100%
          height 100%
          text-align center
          .img-category-item
            margin-top .2rem
            width 1.1rem
            height 1.1rem
          .keyword-category-item
            position absolute
            bottom 0
            width 100%
            height 0.28rem
            text-align center
</style>
