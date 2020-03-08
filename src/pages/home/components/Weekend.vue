<template>
  <div>
    <div class="weekend-title">周末去哪儿</div>
    <ul>
      <li class="weekend-item border-bottom" v-for="item of recommendList" :key="item.recId">
        <div class="week-img-wrapper">
          <img class="week-img" :src="item.recUrl" />
        </div>
        <div class="week-info">
          <p class="week-title">{{item.recTitle}}</p>
          <p class="week-desc">{{item.recDesc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        recId: '00001',
        recUrl: require('../../../../src/assets/images/weekend-01.jpg'),
        recTitle: '东京',
        recDesc: '💎欢乐畅想💎日本东京半自助5日游💎东京+横滨+富士山+镰仓+江之岛神社,泗乎太安逸.'
      }, {
        recId: '00002',
        recUrl: require('../../../../src/assets/images/weekend-02.jpg'),
        recTitle: '罗马',
        recDesc: '德法意瑞12-14天｜含小费｜罗马深度游+罗浮宫+莎士比亚书店｜赠意式特色餐.'
      }, {
        recId: '00003',
        recUrl: require('../../../../src/assets/images/weekend-03.jpg'),
        recTitle: '日本',
        recDesc: '早定优惠赏樱花大阪+京都6天自由行正点航班✔酒店靠近地铁 赠WIFI+意外险.'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .weekend-title
    line-height: .8rem
    background: #eee
    text-indent: .2rem
    margin-top: .2rem
  .week-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 33.9%
    .week-img
      width: 100%
  .week-info
    padding: .1rem
    .week-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .week-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
</style>
