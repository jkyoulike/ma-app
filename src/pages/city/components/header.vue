<template>
  <div class="header">
    城市选择
    <router-link to='/'>
       <div class="iconfont header-back">&#xe610;</div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style  scoped>
.header{
  position:relative;
  overflow:hidden;
  height: 2rem;
  line-height: 2rem;
  text-align: center;
  color: #fff;
  font-size :.32rem;
  padding-left: 1rem;
}
  .header-back{
    position:absolute;
    top: 0;
    left: 0;
    width: .64rem;
    text-align:center;
    font-size :1rem;
    color:#fff;
  }
</style>