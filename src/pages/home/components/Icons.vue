<template>
  <div class="icons">
    <div class="icon">
      <div class="icon-img">
        <img class="icon-img-content" src="../../../../src/assets/images/icon-piao.png"/>
      </div>
      <p class="icon-desc">热门景点</p>
    </div>
    <div class="icon">
      <div class="icon-img">
        <img class="icon-img-content" src="../../../../src/assets/images/icon-package.png"/>
      </div>
      <p class="icon-desc">度假</p>
    </div>
    <div class="icon">
      <div class="icon-img">
        <img class="icon-img-content" src="../../../../src/assets/images/icon-flight.png"/>
      </div>
      <p class="icon-desc">机票</p>
    </div>
    <div class="icon">
      <div class="icon-img">
        <img class="icon-img-content" src="../../../../src/assets/images/icon-hotel.png"/>
      </div>
      <p class="icon-desc">酒店</p>
    </div>
    <div class="icon">
      <div class="icon-img">
        <img class="icon-img-content" src="../../../../src/assets/images/icon-gand.png"/>
      </div>
      <p class="icon-desc">自由行</p>
    </div>
    <div class="icon">
      <div class="icon-img">
        <img class="icon-img-content" src="../../../../src/assets/images/icon-time.png"/>
      </div>
      <p class="icon-desc">攻略</p>
    </div>
    <div class="icon">
      <div class="icon-img">
        <img class="icon-img-content" src="../../../../src/assets/images/icon-trun.png"/>
      </div>
      <p class="icon-desc">一日游</p>
    </div>
    <div class="icon">
      <div class="icon-img">
        <img class="icon-img-content" src="../../../../src/assets/images/icon-cream.png"/>
      </div>
      <p class="icon-desc">团购</p>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeIcons'
}
</script>
<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .icons
    overflow: hidden
    height: 0
    padding-bottom: 50%
    .icon
      position: relative
      overflow: hidden
      width: 25%
      height: 0
      float: left
      padding-bottom: 25%
      .icon-img
        position: absolute
        top: 0
        left: 0
        right: 0
        bottom: .44rem
        box-sizing: border-box
        padding: .1rem
        .icon-img-content
          height: 100%
          display:block
          margin: 0 auto
      .icon-desc
        position: absolute
        left: 0
        right: 0
        bottom: 0
        height: .44rem
        line-height: .44rem
        text-align: center
        color: $darkTextColor
</style>
