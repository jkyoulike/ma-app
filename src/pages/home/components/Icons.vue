<template>
    <div class="icons">
        <div class="icon">
            <div class="icon-img">
                <img class="icon-img-content" src="@/assets/img/1.png" alt="">
            </div>
            <div class="icons-desc">景点门票</div>
        </div>
        <div class="icon">
            <div class="icon-img">
                <img class="icon-img-content" src="@/assets/img/2.png" alt="">
            </div>
            <div class="icons-desc">滑雪季</div>
        </div>
        <div class="icon">
            <div class="icon-img">
                <img class="icon-img-content" src="@/assets/img/3.png" alt="">
            </div>
            <div class="icons-desc">泡温泉</div>
        </div>
        <div class="icon">
            <div class="icon-img">
                <img class="icon-img-content" src="@/assets/img/4.png" alt="">
            </div>
            <div class="icons-desc">植物园</div>
        </div>
        <div class="icon">
            <div class="icon-img">
                <img class="icon-img-content" src="@/assets/img/5.png" alt="">
            </div>
            <div class="icons-desc">游乐园</div>
        </div>
        <div class="icon">
            <div class="icon-img">
                <img class="icon-img-content" src="@/assets/img/6.png" alt="">
            </div>
            <div class="icons-desc">必游榜单</div>
        </div>
        <div class="icon">
            <div class="icon-img">
                <img class="icon-img-content" src="@/assets/img/8.png" alt="">
            </div>
            <div class="icons-desc">演出</div>
        </div>
        <div class="icon">
            <div class="icon-img">
                <img class="icon-img-content" src="@/assets/img/7.png" alt="">
            </div>
            <div class="icons-desc">城市观光</div>
        </div>
    </div>

</template>
<script>
export default {
  name: 'HomeIcons',
  data (){
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