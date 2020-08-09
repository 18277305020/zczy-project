<template>
  <div class="details">
    <Card>
      <p slot="title">水悦湾楼栋信息</p>

      <div class="flex">
        <img :src="img" class="img" />
        <div class="right-box">
          <Tabs type="card">
            <TabPane label="1#楼">
              <Form :label-width="80">
                <Row :gutter="16">
                  <Col span="12">
                    <FormItem label="单元：">2个</FormItem>
                  </Col>
                    <Col span="12">
                    <FormItem label="电梯数：">3梯3户；3梯4户</FormItem>
                  </Col>
                </Row>
                 <Row :gutter="16">
                  <Col span="12">
                    <FormItem label="建筑类型：">超高层</FormItem>
                  </Col>
                    <Col span="12">
                    <FormItem label="楼层：">94；46层</FormItem>
                  </Col>
                </Row>
              </Form>
            </TabPane>
            <TabPane label="2#楼">
                <Form :label-width="80">
                <Row :gutter="16">
                  <Col span="12">
                    <FormItem label="单元：">2个</FormItem>
                  </Col>
                    <Col span="12">
                    <FormItem label="电梯数：">3梯3户；3梯4户</FormItem>
                  </Col>
                </Row>
                 <Row :gutter="16">
                  <Col span="12">
                    <FormItem label="建筑类型：">超高层</FormItem>
                  </Col>
                    <Col span="12">
                    <FormItem label="楼层：">94；46层</FormItem>
                  </Col>
                </Row>
              </Form>
            </TabPane>
            <TabPane label="3#楼">
                <Form :label-width="80">
                <Row :gutter="16">
                  <Col span="12">
                    <FormItem label="单元：">2个</FormItem>
                  </Col>
                    <Col span="12">
                    <FormItem label="电梯数：">3梯3户；3梯4户</FormItem>
                  </Col>
                </Row>
                 <Row :gutter="16">
                  <Col span="12">
                    <FormItem label="建筑类型：">超高层</FormItem>
                  </Col>
                    <Col span="12">
                    <FormItem label="楼层：">94；46层</FormItem>
                  </Col>
                </Row>
              </Form>
            </TabPane>
          </Tabs>
        </div>
      </div>
    </Card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      img: require("../../assets/img/info.jpg")
    };
  }
};
</script>

<style lang="less" scoped>
.details {
  .flex {
    display: flex;

    .img {
      display: block;
      width: 50%;
      margin-right: 20px;
    }
  }

  .right-box {
    flex: 1;
  }
}
</style>