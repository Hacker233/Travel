<template>
    <div class="header">
        <div class="header-left">
          <div class="iconfont back-icon">&#xe624;</div>
        </div>
        <div class="header-input">
          <span class="iconfont">&#xe632;</span>
          输入城市景点游玩主题
        </div>
        <router-link to="/city">
          <div class="header-right">
            {{this.doubleCity}}
            <span class="iconfont arrow-icon">&#xe6aa;</span>
          </div>
        </router-link>
    </div>
</template>
<script>
import { mapState, mapGetters } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city']),
    ...mapGetters(['doubleCity'])
  },
  // props: {
  //   city: String
  // }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl';
  .header
    display flex
    height: .86rem
    line-height $headerHeight
    background $bgColor
    color #fff
    .header-left
      width .64rem
      float left
      .back-icon
        text-align center
        font-size .4rem
    .header-input
      flex 1
      height .64rem
      color #cccccc
      line-height .64rem
      margin-left .2rem
      margin-top .12rem
      padding-left .2rem
      background #ffffff
      border-radius .1rem
    .header-right
      min-width 1.04rem
      padding 0 .1rem
      float right
      text-align center
      color #ffffff
      .arrow-icon
        margin-left -.04rem
        font-size .3rem
</style>
