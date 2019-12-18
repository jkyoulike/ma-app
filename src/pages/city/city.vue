<template>
  <div>
      <city-header></city-header>
      <city-search ></city-search>
      <city-list :hot='hotCities'
      :cities='cities'></city-list>  
  </div>
</template>

<script>
import CityHeader from './components/header'
import CitySearch from './components/search'
import CityList from './components/list'

import axios from 'axios'
export default {
  name: 'City',
  components:{
      CityHeader,
      CitySearch,
      CityList
  },
  data () {
    return {
      cities: {},
      hotCities: []
    }
  },
  // 通过getCityInfo函数获取city.json里的数据，然后传递给handleGetCityInfoSucc函数
  methods:{
    getCityInfo () {
      axios.get('/api/city.json').then(this.handleGetCityInfoSucc)
    },
    handleGetCityInfoSucc (res) {
      res =res.data
      if(res.ret && res.data){
        const data = res.data
        this.cities = data.cities
        this.hotCities = data.hotCities
      }
      // console.log(res)
    }
  },
  // 在生命周期里调用getCityInfo函数
  mounted () {
    this.getCityInfo()
  }
}
</script>

<style scoped>

</style> 