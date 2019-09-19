<template>
  <div class="wrapper">
  <swiper :options="swiperOption" v-if="showSwiper">
    <!-- slides -->
    <swiper-slide v-for="item of list" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl" />
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  },
  computed: {
    showSwiper () {
      return this.list.length
    }
  }
}
</script>

<style scoped lang="stylus">
  /*   >>> 穿透的意思  */
  .wrapper >>> .swiper-pagination-bullet-active
    background #fff
  .wrapper
    overflow hidden
    width 100%
    height 0
    /*保持图片比例  70%  */
    padding-bottom 70.25%
    background gray
    .swiper-img
      width 100%
</style>
