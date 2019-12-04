<template>
<div>
    <home-header :city='city'></home-header>
    <home-swiper :list='swiperList'></home-swiper>
    <home-icons :list='iconList'></home-icons>
    <home-hot :list='hotList'></home-hot>
    <home-weekend :list='weekendList'></home-weekend>
</div>
</template>

<script>
import HomeHeader from './components/header'
import HomeSwiper from './components/swiper'
import HomeIcons from './components/Icons'
import HomeHot from './components/hot'
import HomeWeekend from './components/weekend'
import axios from  'axios'
export default {
  name: 'Home',
  components:{
      HomeHeader,
      HomeSwiper,
      HomeIcons,
      HomeHot,
      HomeWeekend
  },
  data (){
    return{
      city:'',
      swiperList:[],
      iconList:[],
      HotList:[],
      likeList:[],
      weekendList:[]
    }
  },
  methods:{
    getHomeInfo (){
      axios.get('/api/index.json').then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc(res){
      console.log(res)
      res=res.data
      if(res.ret && res.data){
        const data =res.data
        this.city=data.city
        this.swiperList=data.swiperList
        this.iconList=data.iconList
        this.hotList=data.hotList
        this.weekendList=data.weekendList
      }
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>
<style>
</style>