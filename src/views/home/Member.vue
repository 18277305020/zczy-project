<template>
  <div class="member">
    <Card>
      <p slot="title">置业顾问</p>
      <div class="flex">
        <Button @click="onLeft" type="primary" shape="circle" icon="ios-arrow-back"></Button>
        <div class="content">
          <div class="flex adbox" ref="adBox" :style="{width: `${list.length * 301}px`}">
            <div class="item" v-for="i in list">
              <div class="flex justify">
                <img class="img" :src="i.hand" />
                <div class="user">
                  <div>
                    <span class="name">{{i.name}}</span>
                    <span class="fraction">{{i.fraction}} 分</span>
                  </div>
                  <div class="mat">
                    <Poptip trigger="hover" word-wrap placement="bottom">
                      <div slot="content">
                        <img :src="i.code" class="code-img" />
                      </div>
                      <span class="code">
                        <Icon type="ios-text" />微信号
                      </span>
                    </Poptip>
                    <Poptip trigger="hover" word-wrap placement="bottom">
                      <div slot="content">
                        <h2>
                          <Icon type="ios-call" />
                          {{i.mumber}}
                        </h2>
                      </div>
                      <span class="code mag">
                        <Icon type="ios-call" />电话
                      </span>
                    </Poptip>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <Button @click="onRight" type="primary" shape="circle" icon="ios-arrow-forward"></Button>
      </div>
    </Card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: [
        {
          code: require("../../assets/img/member/c1.jpg"),
          hand: require("../../assets/img/member/u1.jpg"),
          mumber: "18277305020",
          name: "a1",
          fraction: "5.00"
        },
        {
          code: require("../../assets/img/member/c2.jpg"),
          hand: require("../../assets/img/member/u2.jpg"),
          mumber: "18277305020",
          name: "a2",
          fraction: "5.00"
        },
        {
          code: require("../../assets/img/member/c3.jpg"),
          hand: require("../../assets/img/member/u3.jpg"),
          mumber: "18277305020",
          name: "a3",
          fraction: "5.00"
        },
        {
          code: require("../../assets/img/member/c4.jpg"),
          hand: require("../../assets/img/member/u4.jpg"),
          mumber: "18277305020",
          name: "a4",
          fraction: "5.00"
        },
        {
          code: require("../../assets/img/member/c5.jpg"),
          hand: require("../../assets/img/member/u5.jpg"),
          mumber: "18277305020",
          name: "a5",
          fraction: "5.00"
        },
         {
          code: require("../../assets/img/member/c6.jpg"),
          hand: require("../../assets/img/member/u6.jpg"),
          mumber: "18277305020",
          name: "a6",
          fraction: "5.00"
        }
      ],
      index: 0
    };
  },
  methods: {
    onRight() {
      if (this.index < this.list.length - 4) {
        this.index++;
        this.$refs.adBox.style.transform = `translate(-${this.index *
          300}px,0)`;
      }
    },
    onLeft() {
      if (this.index > 0) {
        this.index--;
        this.$refs.adBox.style.transform = `translate(-${this.index *
          300}px,0)`;
      }
    }
  }
};
</script>

<style lang="less" scoped>

.member {
  width: 1280px;
  .flex {
    display: flex;
    align-items: center;

    .content {
      flex: 1;
      overflow: hidden;

      .adbox {
        transition: 0.3s;
      }

      .img {
        display: block;
        width: 60px;
        height: 60px;
        border: 1px solid #e7e7e7;
        margin-right: 20px;
        border-radius: 50%;
        background: chartreuse;
      }

      .item {
        width: 300px;
        border-right: 1px solid #e7e7e7;
      }

      .justify {
        justify-content: center;
      }
    }
  }
}

.user {
  .name {
    font-weight: bold;
    font-size: 16px;
  }

  .fraction {
    margin-left: 20px;
    color: red;
  }

  .code {
    border: 1px solid #e7e7e7;
    padding: 4px;
    border-radius: 4px;
    cursor: pointer;

    i {
      font-size: 24px;
    }
  }

  .mag {
    margin-left: 6px;
  }

  .mat {
    margin-top: 10px;
  }

  .code-img {
    width: 200px;
    height: 200px;
  }
}
</style>