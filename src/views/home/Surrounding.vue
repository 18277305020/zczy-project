<template>
  <div class="Surrounding">
    <Card>
      <p slot="title">周边推荐</p>

      <div class="flex">
        <div class="li" v-for="i in 10">
          <Card dis-hover>
            <div class="item">
              <div class="img"></div>
              <div>
                <div class="name">华润</div>
                <div class="pl">170万元</div>
                <div class="txt">3室2厅，89平米</div>
                <div class="name">何庆鹏</div>
              </div>
            </div>
          </Card>
        </div>
      </div>
    </Card>
  </div>
</template>

<script>
export default {};
</script>

<style lang="less" scoped>
.Surrounding {
  .flex {
    display: flex;
    flex-wrap:wrap;
    justify-content: space-between;

    .li{
        width: 19%;
        margin-bottom: 10px;
    }

    .item {
      display: flex;
      width: 100%;

      .img {
        width: 50%;
        height: 80px;
        margin-right: 10px;
        background: chocolate;
      }

      .name{
          font-weight: bold;
      }
      
      .pl{
          color: red;
      }

      .txt{
          font-size: 12px;
          color: #777;
      }
    }
  }
}
</style>