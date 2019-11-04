<template>
  <div id="app">
    <div class="header">
      <div class="header-left"><span class="iconfont">&#xe610;</span></div>
      <div class="header-input">
        <input type="text">
      </div>
    </div>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
body{
  margin: 0;
  padding: 0;
}
.header{
  height: 3rem;
  background:rgb(88, 208, 245);
}
.header-left{
  float: left;
}
.header-left .iconfont{
  font-size: 24px;
  fill: aliceblue;
  color: aliceblue;
  margin-left: 1rem;
  margin-right: 1rem;
}
.header-input input{
  height: 2rem;
  width: 10rem;
}
</style>
