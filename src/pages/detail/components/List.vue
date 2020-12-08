<template>
  <div>
    <div class="item" v-for="(item, index) in list" :key="index">
      <div class="item-titile border-bottom">
        <span class="iconfont item-title-icon">&#xe70a;</span>
        {{item.title}}
      </div>
      <div v-if="item.children" class="item-children">
        <detail-list :list="item.children"></detail-list>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailList',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .item-titile
    line-height: .8rem
    padding: 0 .2rem
    font-size: .32rem
    .item-title-icon
      background-color: $bgColor
  .item-children
    padding: 0 .2rem
</style>
