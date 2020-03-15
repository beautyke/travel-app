<template>
  <div>
    <div class="recommend-title">热销推荐</div>
    <ul>
      <router-link
        :to="'/detail/' + item.recId"
        tag="li"
        class="recommend-item border-bottom"
        v-for="item of recommendList"
        :key="item.recId"
      >
        <img class="item-img" :src="item.recUrl" />
        <div class="item-info">
          <p class="item-title">{{item.recTitle}}</p>
          <p class="item-desc">{{item.recDesc}}</p>
          <button class="item-btn">查看详情</button>
        </div>
      </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    recommendList: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommend-title
    line-height: .8rem
    background: #eee
    text-indent: .2rem
    margin-top: .2rem
  .recommend-item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 2.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-btn
        margin-top: .2rem
        background: #ff9300
        padding: 0 .1rem
        border-radius: .06rem
        color: #fff
</style>
