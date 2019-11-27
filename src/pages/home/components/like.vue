<template>
  <div>
    <div class="title">
      <img class="title-img" src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png" />
      <span class="title-content">猜你喜欢</span>
    </div>
    <ul>
      <li class="item" v-for='item of likeList' :key='item.id'>
        <img class="item-img" :src="item.imgUrl" >
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p>
            <span class="iconfont" v-html='item.star'>{{item.star}}</span >
            <!--因为data里返回的数据类型并不会直接识别为代码，所有我们需要用到v-html来识别星星的的代码-->
            <span class="item-comment">{{item.comment}}</span>
          </p>
          <p class="item-price"><em>¥</em>{{item.price}}<span>起</span></p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
  
    </ul>
  </div>
</template>
<script>
export default {
  name:'HomeLiked',
  data () {
    return {
      likeList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
        title: '上海迪士尼乐园',
        star:'&#xe6b0;&#xe6b0;&#xe6b0;&#xe6b0;&#xe6b0;',
        comment:'277442条评论',
        price: '394',
        desc: '全球最大的迪士尼城堡'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/tuan/team2/1507/2c/83e0e0e7ae082a.jpg_200x200_6d7378b2.jpg',
        title: '东方明珠',
        star:'&#xe6b0;&#xe6b0;&#xe6b0;&#xe6b0;&#xe6b0;',
        comment:'87877条评论',
        price: '80',
        desc: '259米透明悬空观光廊了解一下~'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1906/19/19b7939928a0200da3.img.jpg_200x200_6879c7f7.jpg',
        title: '上海海昌海洋公园',
        star:'&#xe6b0;&#xe6b0;&#xe6b0;&#xe6b0;&#xe6b0;',
        comment:'25826条评论',
        price: '139',
        desc: '全球最大的迪士尼城堡'
      }, {
        id: '004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
        title: '上海迪士尼乐园',
        star:'&#xe6b0;&#xe6b0;&#xe6b0;&#xe6b0;&#xe6b0;',
        comment:'277442条评论',
        price: '394',
        desc: '全球最大的迪士尼城堡'
      },  {
        id: '005',
        imgUrl: 'http://img1.qunarzz.com/tuan/team2/1507/2c/83e0e0e7ae082a.jpg_200x200_6d7378b2.jpg',
        title: '东方明珠',
        star:'&#xe6b0;&#xe6b0;&#xe6b0;&#xe6b0;&#xe6b0;',
        comment:'87877条评论',
        price: '80',
        desc: '259米透明悬空观光廊了解一下~'
      }, {
        id: '006',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1906/19/19b7939928a0200da3.img.jpg_200x200_6879c7f7.jpg',
        title: '上海海昌海洋公园',
        star:'&#xe6b0;&#xe6b0;&#xe6b0;&#xe6b0;&#xe6b0;',
        comment:'25826条评论',
        price: '139',
        desc: '全球最大的迪士尼城堡'
      }
      ]
    }
  }
}
</script>

<style  scoped>
.title{
    margin-top: .2rem;
    background: #eee;
    padding: .2rem;
    height: 2rem;
}
.title-img{
    width: 2rem;
    height: 2rem;
}
.title-content{
      margin-left: .08rem;
      height: .44rem;
      color: red;
      font-size: .32rem;
      line-height: .44rem;
}
</style>