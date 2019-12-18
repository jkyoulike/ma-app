<template>
  <div class="list">
    <div class="area">
       <div class="title border-topbottom">当前城市</div>
       <div class="button-list">
         <div class="button-wrapper">
            <div class="button">北京</div>
         </div>
       </div>
    </div>
    <div class="area">
       <div class="title border-topbottom">热门城市</div>
         <div class="button-list">
         <div class="button-wrapper"
         v-for="item of hot" 
              :key="item.id">
            <div class="button">{{item.name}}</div>
         </div>
       </div>
    </div>
    <div class="area" v-for="(item,key) of cities" :key="key">
       <div class="title border-topbottom">{{key}}</div>
       <div class="item-list">
         <div class="item border-bottom" v-for="itee of item" :key="itee.id">
           {{itee.name}}
         </div>
       </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CityList',
  props: {
      hot:Array,
      cities:Object
  },
}
</script>

<style  scoped>
  .border-topbottom:before{
      border-color: #ccc
  }
    .border-topbottom:after{
      border-color: #ccc
  }
  .border-bottom:after{
      border-color: #ccc;
  }
  .title{
    line-height :2rem;
    background: #eee;
    padding-left :.2rem;
    color: #666;
    font-size: .26rem;
  }
  .button-list{
    overflow: hidden;
    padding: .1rem .6rem .1rem .1rem;
  }
    .button-wrapper{
      float:left;
      width:33.33%;
    }
      .button{

        text-align: center;
        margin :.1rem;
        padding :.1rem 0;
        border: 0.2rem solid #ccc;
        border-radius: .8rem;
      }
    .item{
      line-height: 2rem;
    }
</style>