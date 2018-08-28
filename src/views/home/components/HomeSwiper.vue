<!-- 轮播图 -->
<template>
  <div class="wrap">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
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
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1808/b0/a123fba6d7e3dd02.jpg_750x200_1425741a.jpg'
      },
      {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1808/18/2dbce82b07a23402.jpg_750x200_14356b03.jpg'
      },
      {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/bd/8e4a1c3f470d3702.jpg_750x200_f1f0a8c7.jpg'
      },
      {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1808/b0/a123fba6d7e3dd02.jpg_750x200_1425741a.jpg'
      },
      {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1808/ad/1d2e0030d4ff7302.jpg_750x200_bf5a325d.jpg'
      }
      ]
    }
  },

  components: {},

  computed: {},

  methods: {}
}
</script>
<style lang='stylus' scoped>
  .wrap >>> .swiper-pagination-bullet-active
    background #fff !important
  .wrap
    overflow hidden
    width 100%
    height 0
    padding-bottom 26%
    .swiper-img
      width 100%
</style>
