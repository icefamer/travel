<template>
  <div>
    <div class="banner" @click="handleBannerClick()">
      <img src="//img1.qunarzz.com/sight/p0/1511/d2/d2aec2dfc5aa771290.water.jpg_600x330_cbd1e1e9.jpg" alt="" class="banner-img">
      <div class="banner-info">
        <div class="banner-title">大连海洋世界</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe656;</span>
          39
        </div>
      </div>
    </div>
    <common-gallary
    :imgs="imgs"
    v-show="showGallary"
    @close="handleGallaryClose()"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1511/d2/d2aec2dfc5aa771290.water.jpg_r_800x800_87ef5b1b.jpg',
        'http://img1.qunarzz.com/sight/p0/1511/11/119129bba8323f0d90.water.jpg_r_800x800_0f07ddeb.jpg']
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position relative
    overflow hidden
    height 0
    padding-bottom 55%
    .banner-img
      width 100%
    .banner-info
      display flex
      position absolute
      left 0
      right 0
      bottom 0
      line-height .6rem
      color #ffffff
      background-image linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, .8))
      .banner-title
        flex 1
        font-size .32rem
        padding 0 .2rem
      .banner-number
        padding 0 .4rem
        margin-top .14rem
        line-height .4rem
        height .36rem
        border-radius .2rem
        background-color rgba(0, 0, 0, .8)
        font-size .24rem
        .banner-icon
          font-size .24rem
</style>
