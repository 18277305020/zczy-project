<template>
  <div>
    <Card class="Type">
      <p slot="title">水悦湾户型</p>
      <p slot="extra">
        <a href="#">三层（6）</a>
        <Divider type="vertical" />
        <a href="#">四层（2）</a>
        <Divider type="vertical" />
        <a href="#">更多</a>
      </p>

      <!-- 户型图 -->
      <div class="list">
        <div class="item" v-for="i in list" @click="onItem(i)">
          <Card class="card">
            <img class="img" :src="i.src" />
            <div class="flex foot">
              <span class="label">{{i.name}}</span>
              <span class="centent">{{i.content}}</span>
            </div>
            <Tag color="red">阳台</Tag>
            <Tag color="volcano">通透</Tag>
          </Card>
        </div>
      </div>
    </Card>

    <Modal v-model="modal" footer-hide width="600px">
      <p>
          <img :src="row.src" class="show-img">
      </p>
    </Modal>
  </div>
</template>

<script>
export default {
  data() {
    return {
      modal: false,
      row:{},
      list: [
        {
          src: require("../../assets/img/member/t1.jpg"),
          name: "a1",
          content: "5.00"
        },
        {
          src: require("../../assets/img/member/t2.jpg"),
          name: "a1",
          content: "5.00"
        },
        {
          src: require("../../assets/img/member/t3.jpg"),
          name: "a1",
          content: "5.00"
        },
        {
          src: require("../../assets/img/member/t4.jpg"),
          name: "a1",
          content: "5.00"
        }
      ]
    };
  },
  methods:{
      onItem(i){
          console.log(i)
          this.row = i
          this.modal = true
      }
  }
};
</script>

<style lang="less" scoped>
.Type {
  .list {
    display: flex;
  }

  .item {
    margin: 0 10px;
    width: 25%;

    .img {
      width: 100%;
      height: 240px;
      background: chocolate;
    }

    .flex {
      display: flex;
      justify-content: space-between;
    }

    .foot {
      padding: 10px 0;
    }

    .label {
      font-size: 14px;
      font-weight: bold;
    }
  }
}

.card {
  cursor: pointer;
}

.show-img{
    width: 100%;
}
</style>