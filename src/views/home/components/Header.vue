<!-- 首页头部 -->
<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont backicon">&#xe624;</span>
    </div>
    <div class="header-content">
      <span class="iconfont">&#xe632;</span>
      <p class="p-inline">输入城市/景点/游玩主题</p>
    </div>
    <div class="header-right">
      <p class="p-inline">城市</p>
      <span class="iconfont">&#xe64a;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: '',
  data () {
    return {
    }
  },

  components: {},

  computed: {},

  methods: {}
}

</script>
<style lang='stylus' scoped>
  @import '~styles/varibles.styl';
  .header
    display flex
    height .88rem
    line-height .88rem
    text-align center
    background-color $bgColor
    color #fff
    .header-left
      width .64rem
      margin-left .2rem
      float left
      .backicon
        text-align center
        font-size .36rem
    .header-content
      position relative
      flex 1
      height .64rem
      line-height .64rem
      background #fff
      margin-top .12rem
      margin-left .2rem
      padding-left 0.2rem
      border-radius .06rem
      color #cccccc
      span
        position absolute
        top 0
        left 0.1rem
      .p-inline
        position absolute
        top 0
        left .5rem
    .header-right
      width 1.24rem
      float right
      text-align center
      span
        font-size .24rem
        margin-left .07rem
      .p-inline
        display inline-block
</style>
