<template>
  <ul class="list" >
    <li
      class="item"
      v-for="item of letters"
      :key="item"
      :ref="item"
      @click="handleLetterClick"
      @touchstart="handleTouchStart"
      @touchmove="handleTouchMove"
      @touchEnd="handletouchEnd">
      {{item}}
    </li>
  </ul>
</template>

<script>
export default {
  name: 'CityAlphabet',
  props: {
    cities: Object
  },
  data () {
    return {
      touchStatus: false,
      startY: 0
    }
  },
  updated () {
    this.startY = this.$refs['A'][0].offsetTop
  },
  // 构建出名叫letters的计算机属性
  computed: {
    letters () {
      const letters = []
      for (let i in this.cities) {
        letters.push(i)
      }
      return letters
    }
  },
  methods: {
    handleLetterClick (e) {
      // 向外触发事件change，事件携带的内容e.target.innerText
      this.$emit('change', e.target.innerText)
    },
    handleTouchStart () {
      this.touchStatus = true
    },
    handleTouchMove (e) {
      if (this.touchStatus) {
        // 首先获得A字母距离顶部的高度，然后滑动的时候，看当前的手指距离顶部的高度，然后做差值，就能算出当前手指位置和A这个顶部的差值在除以字母高度，就可以知道当前是第几个字母，然后取对应的字母，触发一个change事件给外部。
        //  拿到A距离顶部的高度
        // const startY = this.$refs['A'][0].offsetTop
        // 拿到手指距离最顶部高度，再减去顶部和搜索框高度79px
        const touchY = e.touches[0].clientY - 79
        // 做差值，除每个字母高度，然后再用Math.floor向下取个整
        const index = Math.floor(touchY - this.startY) / 20
        if (index >= 0 && index < this.letters.length) {
          this.$emit('change', this.letters[index])
        }
      }
    },
    handletouchEnd () {
      this.touchStatus = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .list
    display: flex
    flex-direction: column
    justify-content: center
    position: absolute
    top: 1.58rem
    right: 0
    bottom: 0
    width: .4rem
    .item
      line-height: .4rem
      text-align: center
      color: $bgColor
</style>
