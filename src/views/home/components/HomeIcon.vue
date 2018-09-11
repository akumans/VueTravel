<!-- 导航图标 -->
<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img :src="item.imgUrl" class="icon-imgcontent" />
          </div>
          <p class="icon-desc">{{ item.icontext }}</p>
        </div>
        </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcon',
  data () {
    return {
      iconList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        icontext: '景点门票'
      },
      {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png',
        icontext: '游乐场'
      },
      {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/6a/45f595250c73d102.png',
        icontext: '夏日玩水'
      },
      {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
        icontext: '海洋馆'
      },
      {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
        icontext: '动物植物园'
      },
      {
        id: '0006',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/b1/528a9e80403b8c02.png',
        icontext: '玩转长隆'
      },
      {
        id: '0007',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png',
        icontext: '城市观光'
      },
      {
        id: '0008',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/27/dac2bcf9added702.png',
        icontext: '海滨沙滩'
      },
      {
        id: '0009',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/27/dac2bcf9added702.png',
        icontext: '海滨沙滩'
      }
      ]
    }
  },

  components: {},

  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  },

  methods: {}
}

</script>
<style lang='stylus' scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .icons >>> .swiper-container
    width 100%
    height 0
    margin-top .15rem
    padding-bottom 50%
  .icon
    position relative
    float left
    width 25%
    height 0
    padding-bottom 21%
    .icon-img
      position absolute
      top 0
      left 0
      right 0
      box-sizing border-box
      padding .1rem
      bottom .44rem
      .icon-imgcontent
        display block
        margin 0 auto
        height 100%
    .icon-desc
      position absolute
      left 0
      right 0
      bottom 0
      height .44rem
      font-size .25rem
      line-height .44rem
      text-align center
      color $darkTextColor
      ellipsis()
</style>
