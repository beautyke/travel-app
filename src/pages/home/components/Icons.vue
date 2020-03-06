<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.iconId">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.iconUrl"/>
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconsList: [{
        iconId: '001',
        iconUrl: require('../../../../src/assets/images/icon-piao.png'),
        desc: '热门景点'
      }, {
        iconId: '002',
        iconUrl: require('../../../../src/assets/images/icon-flight.png'),
        desc: '机票'
      }, {
        iconId: '003',
        iconUrl: require('../../../../src/assets/images/icon-package.png'),
        desc: '度假'
      }, {
        iconId: '004',
        iconUrl: require('../../../../src/assets/images/icon-hotel.png'),
        desc: '酒店'
      }, {
        iconId: '005',
        iconUrl: require('../../../../src/assets/images/icon-trun.png'),
        desc: '自由行'
      }, {
        iconId: '006',
        iconUrl: require('../../../../src/assets/images/icon-cream.png'),
        desc: '攻略'
      }, {
        iconId: '007',
        iconUrl: require('../../../../src/assets/images/icon-strategy.png'),
        desc: '一日游'
      }, {
        iconId: '008',
        iconUrl: require('../../../../src/assets/images/icon-place.png'),
        desc: '跟团游'
      }, {
        iconId: '009',
        iconUrl: require('../../../../src/assets/images/icon-love.png'),
        desc: '泡温泉'
      }, {
        iconId: '010',
        iconUrl: require('../../../../src/assets/images/icon-phone.png'),
        desc: '门票'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconsList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .icons >>> .swiper-container
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
