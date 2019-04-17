<template>
  <div>
    <div
      class="banner"
      @click="handleBannerClick"
    >
      <img
        class="banner-img"
        src="//img1.qunarzz.com/sight/p0/1604/1e/1e75f8e1af9fe81f90.img.jpg_600x330_aeba2c96.jpg"
        alt=""
      >
      <div class="banner-info">
        <div class="banner-title">大连圣亚海洋世界(AAAA景区)</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe689;</span>39
        </div>
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGallaryClick"
    ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data() {
    return {
      showGallary: false,
      imgs: [
        'https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=3063548377,1984410721&fm=26&gp=0.jpg',
        'https://ss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=187658256,3610838439&fm=26&gp=0.jpg'
      ]
    }
  },
  methods: {
    handleBannerClick() {
      this.showGallary = true
    },
    handleGallaryClick() {
      this.showGallary = false
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
    line-height 0.6rem
    color #ffffff
    background-image linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
    .banner-title
      flex 1
      font-size 0.32rem
      padding 0 0.2rem
    .banner-number
      padding 0 0.4rem
      height 0.32rem
      margin-top 0.14rem
      line-height 0.32rem
      border-radius 0.2rem
      background rgba(255, 0, 0, 0.8)
      font-size 0.24rem
      .banner-icon
        font-size 0.24rem
</style>
