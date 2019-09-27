<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img alt='you name' class="banner-img" src="https://img1.qunarzz.com/vs_ceph_vs_tts/e6503621-e200-4b13-8822-f68b0625cb17.jpg_r_640x420x90_169cb653.jpg" />
      <div class="banner-info">
        <div class="banner-tittle">
          大连海洋世界(AAAA)
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe692;</span>
          39
        </div>
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGallaryClose"
    ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://m.kstjkq.com/templets/default/shouji/images/banner/zhaomu.jpg', 'http://m.kstjkq.com/templets/default/shouji/images/banner/zhaomu.jpg']
    }
  },
  components: {
    CommonGallary
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  }
}
</script>

<style lang='stylus' scoped>
  .banner
    position relative
    overflow: hidden
    height 0
    padding-bottom 55%
    .banner-img
      width 100%
    .banner-info
      display flex
      position:absolute
      left:0
      right 0
      bottom 0
      line-height .6rem
      color #fff
      background-image :linear-gradient(top, rgba(0,0,0,0), rgba(0,0,0,0.8))
      .banner-tittle
        flex 1
        font-size:.32rem
        padding:0 .2rem
      .banner-number
        padding 0 .4rem
        margin-top .14rem
        height .32rem
        line-height .32rem
        border-radius: .2rem
        background:rgba(0,0,0,.8)
        font-size .24rem
        .banner-icon
          font-size .24rem
</style>
