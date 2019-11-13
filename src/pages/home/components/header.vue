<template>
  <div id="app">
    <div class="header">
      <div class="header-left">
          <div class="iconfont">&#xe610;</div>
      </div>
      <div class="header-input">
        <span class="iconfont">&#xe647;</span> 输入城市/景点/游玩主题
      </div>
      <div class="header-righe">城市
      <span class="iconfont">&#xe736;</span>
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
  background:#00afc7;
  line-height:4rem;
  display:flex;
}
.header-left{
  float: left;
  width:2rem;
  color:#fff;
  margin-left:1rem;
}
.header-input{
  height:2rem;
  line-height:2rem;
  color:#ccc;
  flex:1;
  background:#fff;
  margin-top:1rem;
  border-radius:5px;
}
.header-righe{
  margin:0rem 1rem 0rem 1rem;
  color:#fff;
  font-weight:bold;
  font-family:"宋体";
}

</style>