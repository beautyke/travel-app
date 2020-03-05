<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
            <swiper-slide>
                <img class="swiper-img" src="../../../../src/assets/images/swiper-01.jpg"/>
            </swiper-slide>
            <swiper-slide>
                <img class="swiper-img" src="../../../../src/assets/images/swiper-02.jpg"/>
            </swiper-slide>
            <swiper-slide>
                <img class="swiper-img" src="../../../../src/assets/images/swiper-03.jpg"/>
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
      }
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
    padding-bottom: 31.25%
    background: #eee
    .swiper-img
        width: 100%
</style>
