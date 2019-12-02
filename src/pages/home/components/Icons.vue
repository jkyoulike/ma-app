<template>
    <div class="icons">
        <swiper :options="swiperOption">
            <swiper-slide v-for='(page, index) of pages' :key='index'>
        <div class="icon"  v-for="item of page" :key="item.id">
            <div class="icon-img">
                <img class="icon-img-content" :src="item.imgUrl" alt="">
            </div>
            <div class="icons-desc">{{item.desc}}</div>
        </div>
            </swiper-slide>
        </swiper>
    </div>

</template>
<script>
export default {
  name: 'HomeIcons',
  props:{
    list:Array
  },
  data (){
      return{
        swiperOption:{
          autoplay:false
        }
    }
},
computed: {
    pages () {
      const pages = []
      this.list.forEach((item, index) => {
        //index是图标数组的索引，利用索引除以8来计算是否分页
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style scoped>
.icons{
    overflow: hidden;
    height: 0;
    padding-bottom:50%;
}
.icon{
    position: relative;
    overflow: hidden;
    float: left;
    width: 25%;
    height: 0;
    padding-bottom: 25%;
    background: #fff;
}
.icon-img{
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: .44rem;
    box-sizing: border-box;
}
.icon-img-content{
    display: block;
    margin: 0 auto;
    height: 90%;
}
.icons-desc{
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    text-align: center;
    font-size: .2rem;
}
</style>