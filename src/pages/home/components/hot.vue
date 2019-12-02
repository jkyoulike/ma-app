<template>
  <div>
      <div class="title">
        <img class="title-img" src="http://img1.qunarzz.com/piao/fusion/1711/16/bfbb9874e8f11402.png">
        <span class='title-left'>本周热门榜单</span>
        <span class="title-right">全部榜单 ></span>
        </div>
        <div class="wrapper">
          <swiper :options='swiperOption'>
              <swiper-slide v-for='item of list' :key='item.id'>
                  <div class="hot-img">
                    <img class="hot-img-content" :src="item.imgUrl" />
                  </div>  
                    <p class="desc">{{item.desc}}</p>
                    <p class="price">{{item.price}}<span>起</span></p>
              </swiper-slide>
          </swiper>
      </div>
  </div>
</template>

<script>
export default {
  name:'HomeHot',
  props:{
    list:Array
  },
  data () {
      return{
          swiperOption:{
                slidesPerView : 3.5,
                centeredSlides : false,
          },
      }
  }
  }

</script>

<style  scoped>
.title{
    position: relative;
    padding: .2rem;
    padding-bottom: -.1rem;
}
.title-left{
    font-size: .32rem;
    line-height: .44rem;
}
.title-right{
    float: right;
    color: #616161;
    font-size: .24rem;
    line-height: .28rem;
    position: absolute;
    top: .80rem;
    right: .32rem;;
}
.title-img{
    display: inline-block;
    overflow: hidden;
    width:1.5rem;;
    height:1.5rem;
    vertical-align: top;
}
.wrapper{
    height: 0;
    padding-bottom: 40%;
    overflow: hidden;
    width: 100%;
}
.hot-img{
    overflow: hidden;
    height: 24%;
    margin-top: -.2rem;
}
.hot-img-content{
    margin: .15rem;
    width: 100%;
}
.desc{
    margin: 0;
    text-align: center;
    font-size: .24rem;
    line-height: .32rem;
    color: #212121;
}
.price{
    text-align: center;
    color: #ff8300;
    font-size: .24rem;
    line-height: .32rem;
}
span{
    color: #212121;
    font-size: .24rem;
}
</style>