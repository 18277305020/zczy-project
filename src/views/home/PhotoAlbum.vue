<template>
  <div class="photo">
    <Card>
      <p slot="title">水悦湾楼盘相册</p>
      <p slot="extra">
        <a href="#">户型（6）</a>
        <Divider type="vertical" />
        <a href="#">交通图（2）</a>
        <Divider type="vertical" />
        <a href="#">实景图（6）</a>
        <Divider type="vertical" />
        <a href="#">效果图（2）</a>
        <Divider type="vertical" />
        <a href="#">样板间（6）</a>
        <Divider type="vertical" />
        <a href="#">活动现场（2）</a>
        <Divider type="vertical" />
        <a href="#">配套图（6）</a>
        <Divider type="vertical" />
        <a href="#">更多</a>
      </p>

      <div class="alb">
        <div class="item" v-for="i in 5">
          <img class="img" :src="img" />
          <p>南宁宝能</p>
        </div>
      </div>
    </Card>
  </div>
</template>

<script>
export default {
    data(){
        return{
            img:require('../../assets/img/banner.jpg')
        }
    }
};
</script>

<style lang="less" scoped>
.photo {

  .alb {
    display: flex;
    justify-content: space-between;
  }

  .item {
    width: 19%;
    text-align: center;
  }

  .img {
    width: 100%;
    height: 200px;
    margin-bottom: 10px;
    background: chocolate;
  }
}
</style>