<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img
        class="banner-img"
        src="https://imgs.qunarzz.com/vs_ceph_vs_tts/1162def6-3422-4170-952d-9feb82fb0b14.jpg_r_390x260x95_4b30f88c.jpg"
      />
      <div class="banner-info">
        <div class="banner-title">好奇宝贝“泰”开心·亲近动物学知识</div>
        <div class="banner-number">
          <span class="iconfont banner-icon"><font-awesome-icon icon="image" /></span>10
        </div>
      </div>
    </div>
    <common-gallery :imgs="imgs" v-show="showGallery" @close="handleGalleryClose"></common-gallery>
  </div>
</template>

<script>
import CommonGallery from 'common/gallery/Gallery'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallery: false,
      imgs: ['https://imgs.qunarzz.com/p/tts6/1710/59/8bfbb77ea973c802.jpg_r_390x260x95_ad426efb.jpg',
        'https://imgs.qunarzz.com/p/tts8/1710/67/2f6fa9c23fd4f502.jpg_r_390x260x95_d6564f59.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallery = true
    },
    handleGalleryClose () {
      this.showGallery = false
    }
  },
  components: {
    CommonGallery
  }
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
        margin-top: .14rem
        padding: 0 .4rem
        line-height: .32rem
        height: .32rem
        border-radius: .2rem
        background: rgba(0,0,0,.8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
