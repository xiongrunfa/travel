<template>
  <div class="weekend">
    <div class="title">
      周末去哪儿
    </div>
    <ul>
      <li class="item" v-for="item in weekendList" :key="item.id">
          <div class="item-img-wrapper">
            <img :src="item.imgUrl" class="item-img">
          </div>
          <div class="item-info">
             <p class="info-title">{{item.title}}</p>
             <p class="info-desc">{{item.desc}}</p>
          </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    weekendList: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import  '~styles/mixins.styl'
  @import  '~styles/varibles.styl'
  .weekend
    background-color: #f5f5f5
    .title
      padding: .24rem 0 .26rem .26rem
    .item
      background-color: #fff
      margin-bottom: .1rem
      .item-img-wrapper
        overflow: hidden
        height: 0
        padding-bottom: 37.09%
        .item-img
          width: 100%
      .item-info
        padding: 0 0 .2rem .2rem
        min-width: 0
        .info-title
           margin-top: .2rem
           font-size: .28rem
           color: $darkTextColor
           ellipsis()
        .info-desc
           margin-top: .2rem
           color: #616161
           font-size: .24rem
           ellipsis()
</style>
