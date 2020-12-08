<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe639;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe606;</span>
      输入城市/景点/游玩主题
      </div>
    <router-link to="/city">
      <div class="header-right">
       {{this.city}}
      <span class="iconfont arrow-icon">&#xe6aa;</span>
     </div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'Header',
  computed: {
    ...mapState(['city'])
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
     display: flex
     line-height: $headerHeight
     background: $bgColor
     color: #fff
     .header-left
        width: .64rem
        float: left
        .back-icon
          font-size: .4rem
          text-align: center
     .header-input
        flex: 1
        height: .64rem
        line-height: .64rem
        background: #fff
        margin-top: .12rem
        margin-left: .2rem
        padding-left: .2rem
        border-radius: .1rem
        color: #ddd
      .header-right
         box-sizing: border-box
         overflow: hidden
         min-width: 1.28rem
         float: right
         text-align: center
         padding: 0 .22rem
         color: #fff
         .arrow-icon
           width: .28rem
           margin-left: -.05rem
           font-size: .28rem
</style>
