<!-- 首页 -->
<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icon></home-icon>
  </div>
</template>

<script>
import HomeHeader from './components/HomeHeader'
import HomeSwiper from './components/HomeSwiper'
import HomeIcon from './components/HomeIcon'
export default {
  name: 'Home',
  data () {
    return {
    }
  },

  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcon
  },

  computed: {},

  methods: {}
}

</script>
<style lang='stylus' scoped>

</style>
