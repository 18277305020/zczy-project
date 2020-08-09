<template>
  <div class="info">
    <Card class="dynamic">
      <p slot="title">水悦湾楼盘动态</p>
      <a href="#" slot="extra">更多动态</a>

      <!-- list文本 -->
      <div class="list">
        <div v-for="i in 4" class="item">
          <div class="hand">
            <Tag color="red">动态</Tag>
            <span class="lable">标题标题标题标题标题标题标题标题标题标题标题标题</span>
            <span class="time">2020-08-08</span>
          </div>
          <div class="content">
            <span
              class="text"
            >正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文正文</span>
            <a>阅读全文</a>
          </div>
        </div>
      </div>
    </Card>
    <Card class="story">
      <p slot="title">楼盘故事</p>
      <a href="#" slot="extra">更多</a>

      <!-- 楼盘故事 -->
      <div class="time-line">
        <Timeline>
          <TimelineItem v-for="i in 5">
            <p class="time">
              2020-03-31
              <Tag color="blue">交房</Tag>
            </p>
            <p class="centent">预计2020年8月二期住宅交房预计2020年8月二期住宅交房预计2020年8月二期住宅交房预计2020年8月二期住宅交房</p>
          </TimelineItem>
        </Timeline>
      </div>
    </Card>
  </div>
</template>

<script>
export default {};
</script>

<style lang="less" scoped>
.info {
  display: flex;
  justify-content: space-between;

  .dynamic {
    width: 70%;
    margin-right: 20px;
  }

  .story {
    flex: 1;
  }
}

.list {
  max-height: 400px;
  overflow: auto;
  .item {
    border-bottom: 1px solid #e7e7e7;
    padding-bottom: 10px;
    padding-right: 20px;
    margin-bottom: 10px;

    .hand {
      display: flex;
      align-items: center;
    }

    .content {
      display: flex;
      justify-items: flex-end;
      margin-top: 10px;
    }

    .lable {
      font-size: 16px;
      font-weight: bold;
      margin: 0 20px;
    }

    .time {
      color: #999;
    }

    .text {
      flex: 1;
      color: #555;
      overflow: hidden;

      text-indent: 12px;
      font-size: 12px;
      text-overflow: ellipsis;
      display: -webkit-box;
      -webkit-line-clamp: 1;
      -webkit-box-orient: vertical;
      margin-right: 20px;
    }
  }
}

.time-line {
  max-height: 400px;
  overflow: auto;
  .time {
    color: #777;
  }

  .centent {
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 1;
    -webkit-box-orient: vertical;
  }
}
</style>