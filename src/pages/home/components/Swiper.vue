<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
            <swiper-slide v-for="item of swiperList" :key="item.id">
                <img class="swiper-img" :src="item.imgUrl"/>
            </swiper-slide>
            <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        // 循环轮播
        loop: true
      },
      swiperList: [
        {id: '0001', imgUrl: require('../../../../src/assets/images/swiper-01.jpg')},
        {id: '0002', imgUrl: require('../../../../src/assets/images/swiper-02.jpg')},
        {id: '0003', imgUrl: require('../../../../src/assets/images/swiper-03.jpg')}
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 30.48%
    background: #eee
    .swiper-img
        width: 100%
</style>
