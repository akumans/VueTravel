<!-- 首页 -->
<template>
  <div>
    <home-header></home-header>
    {{hello}}
  </div>
</template>

<script>
import HomeHeader from './components/Header'
export default {
  name: 'Home',
  data () {
    return {
      hello: 'haha'
    }
  },

  components: {
    HomeHeader
  },

  computed: {},

  methods: {}
}

</script>
<style lang='stylus' scoped>

</style>
