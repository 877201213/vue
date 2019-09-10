<template>
  <div>
    <div class="title">
      热销推荐</div>

    <ul>
      <li class="item border-bottom" v-for="item of recommendList"
          :key="item.id">
        <div>
          <img class="item-img" :src="item.imgUrl"/>
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
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
    .item-img-wrapper
      height: 0
      overflow hidden
      padding-bottom 33.9%
      .item-img
        width 100%
    .item-info
      padding .1rem
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #ccc
        ellipsis()
</style>
