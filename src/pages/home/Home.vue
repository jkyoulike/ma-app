<template>
<div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-hot></home-hot> 
</div>
</template>

<script>
import HomeHeader from './components/header'
import HomeSwiper from './components/swiper'
import HomeIcons from './components/Icons'
import HomeHot from './components/hot'
export default {
  name: 'Home',
  components:{
      HomeHeader,
      HomeSwiper,
      HomeIcons,
      HomeHot
  }
}
</script>

<style>
</style>