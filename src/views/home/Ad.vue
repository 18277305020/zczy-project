<template>
  <div class="ad">
    <Row :gutter="20">
      <Col span="12">
        <div class="im">
          <img :src="img" />
        </div>
      </Col>
      <Col span="12">
        <div class="item align-it">
          <div class="title">水悦湾</div>
          <div class="txt">别名：宝能城</div>
        </div>
        <div class="item">
          <Tag color="magenta">magenta</Tag>
          <Tag color="red">red</Tag>
          <Tag color="volcano">volcano</Tag>
          <Tag color="orange">orange</Tag>
          <Tag color="gold">gold</Tag>
          <Tag color="yellow">yellow</Tag>
        </div>
        <div class="item">
          <div class="label">价格：</div>
          <div class="txt">
            <b class="red">17000元</b>/m2起
          </div>
        </div>
        <div class="item">
          <div class="label">主力户型：</div>
          <div class="txt">17000元/m2起</div>
        </div>
        <div class="item">
          <div class="label">项目地址：</div>
          <div class="txt">良庆平乐大道35号</div>
          <a
            class="icon"
            target="view_window"
            href="https://map.baidu.com/poi/%E6%B0%B4%E6%82%A6%E6%B9%BE/@12063008.645318892,2599099.6369795427,12.93z?uid=9ccdda86ccd7c13828201a36&ugc_type=3&ugc_ver=1&device_ratio=1&compat=1&querytype=detailConInfo&da_src=shareurl"
          >
            <Icon type="ios-pin" />查看地图
          </a>
        </div>
        <div class="item">
          <div class="label">近期开盘：</div>
          <div class="txt">良庆平乐大道35号</div>
        </div>
        <div class="item">
          <div class="label">接待中心地址：</div>
          <div class="txt">良庆平乐大道35号</div>
          <a
            class="icon"
            target="view_window"
            href="https://map.baidu.com/poi/%E6%B0%B4%E6%82%A6%E6%B9%BE/@12063008.645318892,2599099.6369795427,12.93z?uid=9ccdda86ccd7c13828201a36&ugc_type=3&ugc_ver=1&device_ratio=1&compat=1&querytype=detailConInfo&da_src=shareurl"
          >
            <Icon type="ios-pin" />查看地图
          </a>
        </div>
        <div class="item">
          <div class="label">咨询电话：</div>
          <div class="txt red">
            <b>良庆平乐大道35号</b>
          </div>
        </div>
      </Col>
    </Row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      img: require("../../assets/img/ad.jpg")
    };
  }
};
</script>

<style lang="less" scoped>
.im {
  width: 100%;
  border-radius: 4px;
  overflow: hidden;
  border: 1px solid #e7e7e7;

  img {
    display: block;
    width: 100%;
    height: 100%;
  }
}

.red {
  color: red;
}

.align-it {
  align-items: flex-end;
}

.ad {
  .item {
    display: flex;
    align-items: center;
    margin-bottom: 20px;

    .title {
      line-height: 30px;
      font-size: 26px;
      font-weight: bold;
    }

    .label {
      font-weight: bold;
      font-size: 16px;
    }

    .txt {
      margin-left: 20px;
      font-size: 16px;
    }

    .icon {
      margin-left: 20px;
      font-size: 12px;
    }
  }
}
</style>