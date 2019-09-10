<template>
  <div>
<div class="title">
  热销推荐</div>

  <ul>
    <li class="item border-bottom" v-for="item of recommendList"
    :key="item.id">
        <img class="item-img" :src="item.imgUrl"/>
      <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        <button class="item-button"> 查看详情</button>
      </div>
    </li>
  </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [ {
        Id: '0001',
        imgUrl: 'http://m.kstjkq.com/uploads/190905/1-1ZZ5142614522.jpg',
        title: '昆山同济口腔医院',
        decs: '昆山首家口腔专科医院'
      }, {
        Id: '0002',
        imgUrl: 'http://m.kstjkq.com/uploads/190708/1-1ZFQG329592.jpg',
        title: '昆山同济口腔医院',
        decs: '昆山首家口腔专科医院'
      }]
    }
  }
}
</script>

<style scoped lang="stylus">
  @import "~styles/mixins.styl"
.title
  margin .2rem 0 0 0
  line-height .8rem
  background #eee
  text-indent .2rem
.item
  overflow hidden
  display flex
  height 1.9rem
  .item-img
    width 1.7rem
    height 1.7rem
    padding .1rem
  .item-info
    flex: 1
    padding .1rem
    min-width: 0
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis()
    .item-desc
      line-height .4rem
      color #ccc
      ellipsis()
    .item-button
      line-height .44rem
      margin-top .16rem
      background #ff9300
      padding 0 .1rem
      border-radius .06rem
      color #fff
      ellipsis()
</style>
