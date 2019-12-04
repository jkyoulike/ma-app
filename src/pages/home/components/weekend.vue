<template>
<div>
    <div class="title">周末去哪儿</div>
        <li class="item border-bottom" v-for="item of list" :key="item.id">
          <div class="item-img-wrapper">
            <img class="item-img" :src="item.imgUrl" >
          </div>
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
          </div>
        </li>
  </div>
</template>
<script>
export default {
  name: 'Weekend',
  props:{
      list:Array
  }
}
</script>
<style scoped>
.title{
    line-height: 2rem;
    background: #eee;
    text-indent:.8rem;
    font-size: 0.4rem
}
.item-img-wrapper{
    width: 100%;
}
.item-img{
    width: 100%;
}
.item{
    list-style: none;
}
.item-title{
    line-height: .62rem;
    margin: .32rem;
}
.item-desc{
    font-size: .42rem;
    color: #ccc;
    overflow: hidden; /*自动隐藏文字*/
    text-overflow: ellipsis;/*文字隐藏后添加省略号*/
    white-space: nowrap;/*强制不换行*/
}
</style>