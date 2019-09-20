<template>
  <div>
    <city-header></city-header>
    <city-search></city-search>
</div>
</template>

<script>
import CityHeader from '@/pages/city/components/Header'
import CitySearch from '@/pages/city/components/Search'
export default {
  name: 'City',
  components: {CitySearch, CityHeader},
  comments: {
    CityHeader,
    CitySearch
  }
}
</script>

<style scoped lang="stylus">

</style>
