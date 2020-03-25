<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.id">
        <div class="item-img-wrapper">
          <img :src="item.imgUrl" class="item-img">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    list: Array
  }
}
</script>

<style scoped lang="stylus">
  @import "~@/assets/styles/mixins.styl"
  .title
    line-height .8rem
    background #eee
    text-indent .2rem
  .item-img-wrapper
    height 0
    overflow hidden
    padding-bottom 37.09%
    .item-img
      width 100%
  .item-info
    padding .1rem
    .item-title
      font-size: .32rem
      ellipsis()
      line-height: .54rem
    .item-desc
      line-height .4rem
      ellipsis()
      color: #ccc
</style>
