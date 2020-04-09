<template>
  <div>
  <detail-banner></detail-banner>
  <detail-header></detail-header>
  <div class="content">
  <detail-list :list="list"></detail-list>
  </div>
  </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList
  },
  data () {
    return {
      list: [{
        title: '成人票',
        children: [{
          title: '成人三项目联票'
        }, {
          title: '成人五项目联票'
        }]
      }, {
        title: '学生票'
      }, {
        title: '童児票'
      }, {
        title: '特売票'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .content
    height: 50rem
</style>
