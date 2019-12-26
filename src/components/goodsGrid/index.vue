<template>
  <div class="card">
    <div class="card-container">
      <div class="card-title">
        <div class="left">人气推荐</div>
        <div class="right">更多 ></div>
      </div>
      <div class="card-main">
        <div class="top-grid"></div>
        <div class="bottom-grid">
          <div class="grid-card" v-for="value in 4" :key="value">
            <div class="grid-hot">预售 魔兽世界编年史同人画集 时光之沙漏</div>
          </div>
          <!-- <van-grid square clickable :column-num="2" :border="false">
            <van-grid-item v-for="value in 4" :key="value">
              
            </van-grid-item>
          </van-grid>-->
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.card {
  margin-top: 10px;
  background: #fff;
  padding: 18px;
  .card-container {
    .card-title {
      display: flex;
      justify-content: space-between;
      align-items: center;
      .left {
        font-size: 15px;
      }
      .right {
        font-size: 13px;
      }
    }
    .card-main {
      margin-top: 10px;
      .bottom-grid {
        display: flex;
        flex-wrap: wrap;
      }
      .grid-card {
        height: 120px;
        width: 50%;
        background-size: cover;
        background: url("https://th.wallhaven.cc/small/39/39gogv.jpg");
      }
    }
  }
}
</style>
