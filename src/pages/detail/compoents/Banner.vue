<template>
  <div class="banner">
    <img class="banner-img" src="../../../../static/images/recommend-01.jpg" />
    <div class="banner-info">
      <div class="banner-title">重庆复古古风小镇</div>
      <div class="banner-number"><span class="iconfont banner-icon">&#xe6ff;</span>6</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailBanner'
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        line-height: .4rem
        margin-top: .14rem
        padding: 0 .4rem
        border-radius: .2rem
        background: rgba(0, 0, 0, 0)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
