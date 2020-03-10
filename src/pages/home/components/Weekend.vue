<template>
  <div>
    <div class="weekend-title">周末去哪儿</div>
    <ul>
      <li class="weekend-item border-bottom" v-for="item of weekendList" :key="item.weekId">
        <div class="week-img-wrapper">
          <img class="week-img" :src="item.weekUrl" />
        </div>
        <div class="week-info">
          <p class="week-title">{{item.weekTitle}}</p>
          <p class="week-desc">{{item.weekDesc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    weekendList: Array
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
    padding-bottom: 66%
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
