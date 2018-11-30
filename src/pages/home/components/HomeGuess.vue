<template>
<div class="guess">
  <div class="youlove">
    <img class="love" :src="loveUrl" alt="">
    <span>猜你喜欢</span>
  </div>
  <scenic-spot v-for="list of scenicList" :key="list.id" :list='list' class="scenic_spot"></scenic-spot>
</div>
</template>

<script>
import ScenicSpot from './ScenicSpot'
export default {
  name: 'HomeGuess',
  components: {
    ScenicSpot
  },
  data () {
    return {
      loveUrl: 'http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png',
      scenicList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1809/5d/5d3bcfd3b565bef1a3.img.jpg_200x200_62b19b3c.jpg',
          scenicSpotName: '观音山梦幻海岸车技演艺秀',
          starsNum: 3,
          commentNum: 3456,
          price: 99,
          place: '思明区',
          showTip: false,
          tip: '',
          tagName: 'today'
        }, {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1711/fe/fe517fa5a183e4bca3.img.jpg_200x200_1afe21c0.jpg',
          scenicSpotName: '厦门老院子景区',
          starsNum: 5,
          commentNum: 1486,
          price: 256,
          place: '集美区',
          showTip: false,
          tip: '',
          tagName: 'today'
        }, {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1506/f6/f6b727f036fe5d6d.water.jpg_200x200_a3c26b4d.jpg',
          scenicSpotName: '鼓浪屿',
          starsNum: 5,
          commentNum: 40905,
          price: 15,
          place: '思明区',
          showTip: true,
          tip: '文艺小清新必去景点~',
          tagName: 'anytime'
        }, {
          id: '0004',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/97/ea51af995c4d4de85c53855302b2f5af.water.jpg_200x200_ee569936.jpg',
          scenicSpotName: '鼓浪屿往返轮渡',
          starsNum: 5,
          commentNum: 26173,
          price: 15,
          place: '鼓浪屿',
          showTip: true,
          tip: '你离鼓浪屿只有一张船票的距离~',
          tagName: 'tomorrow'
        }, {
          id: '0005',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/201309/09/dbde58a394d3bba3c8d65eac.jpg_200x200_db515a0b.jpg',
          scenicSpotName: '双龙潭生态运动景区',
          starsNum: 5,
          commentNum: 612,
          price: 159.8,
          place: '集美区',
          showTip: false,
          tip: '',
          tagName: 'anytime'
        }, {
          id: '0006',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1502/6b/6b079eb07e4b38c9.water.jpg_200x200_6cf885fe.jpg',
          scenicSpotName: '灵玲国际马戏城',
          starsNum: 5,
          commentNum: 5785,
          price: 60,
          place: '集美区',
          showTip: true,
          tip: '以马戏表演为主题集合休闲娱乐的度假区~',
          tagName: 'today'
        }, {
          id: '0007',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1412/da/273e834ab7e13fd5a51751d57d20f828.water.jpg_200x200_89988804.jpg',
          scenicSpotName: '厦门日月谷温泉渡假村',
          starsNum: 5,
          commentNum: 905,
          price: 188,
          place: '海沧区',
          showTip: true,
          tip: '🔥好评如潮，小伙伴热推景点~',
          tagName: 'anytime'
        }, {
          id: '0008',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1703/9f/9f1113c82abd3f83a3.img.jpg_200x200_7db6b8c1.jpg',
          scenicSpotName: '厦门方特东方神画',
          starsNum: 5,
          commentNum: 1558,
          price: 166,
          place: '厦门方特东方神画',
          showTip: false,
          tip: '',
          tagName: 'tomorrow'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .youlove
    width 100%
    height 0.8rem
    line-height 0.8rem
    margin-left 0.16rem
    .love
      width 0.32rem
      height 0.32rem
      margin-top -0.08rem
  .scenic_spot
    margin-left 0.2rem
    margin-top 0.2rem
    padding-bottom 0.2rem
    border-bottom 1px solid #dbdbdb
</style>
