<template>
  <div>
     <Home-Header></Home-Header>
    <Home-Swiper></Home-Swiper>
    <Home-icons></Home-icons>
    <Home-Recommend></Home-Recommend>
    <Home-weekend></Home-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/weekend'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  }}
</script>

<style scoped>

</style>
