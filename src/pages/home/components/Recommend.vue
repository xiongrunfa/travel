<template>
  <div>
    <div class="title">
      <img src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png"
      class="title-img">
      <span class="title-desc">猜你喜欢</span>
    </div>
    <ul>
      <router-link
      tag="li"
      :to="'/detail/' + item.id"
      class="item border-bottom"
      v-for="item in recommendList"
      :key="item.id">
          <img :src="item.imgUrl" class="item-img">
          <div class="item-info">
             <p class="info-title">{{item.title}}</p>
             <p class="info-desc">{{item.desc}}</p>
             <button class="info-btn">查看详情</button>
          </div>
      </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRcommend',
  props: {
    recommendList: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import  '~styles/mixins.styl'
  @import  '~styles/varibles.styl'
  .title
    padding: .24rem 0 .26rem 0
    .title-img
       width: .3rem
       height: .3rem
       vertical-align: top
       margin-left: .2rem
    .title-desc
      display: inline-block
      margin-left: .08rem
      height: .44rem
      color: $darkTextColor
      font-size: .32rem
      line-height: .44rem
  .item
    display: flex
    margin-left: .2rem
    height: 2.2rem
    .item-img
      width: 2rem
      height: 2rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .info-title
         margin-top: .2rem
         font-size: .32rem
         color: $darkTextColor
         ellipsis()
      .info-desc
         margin-top: .1rem
         color: #bbb
         ellipsis()
      .info-btn
        line-height: .44rem
        margin-top: .44rem
        background-color: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
