<template>
  <div class="home">
    <ZNav />
    <div class="swipe">
      <van-swipe :autoplay="3000">
        <van-swipe-item v-for="(item,index) in imgArr" :key="index">
          <div class="swipe-item">
            <img :src="item" alt />
          </div>
        </van-swipe-item>
      </van-swipe>
    </div>
    <div class="grid">
      <van-grid square clickable>
        <van-grid-item
          v-for="(value,index) in iconArr"
          :key="index"
          :icon="value.icon"
          :text="value.txt"
        />
      </van-grid>
    </div>
    <div class="main">
      <ZGoods />
    </div>
  </div>
</template>

<script>
// 导入nav
import ZNav from "@/components/nav";
// 导入商品列表
import ZGoods from "@/components/goodsGrid";
const imgArr = [
  require("@/assets/img1.jpg"),
  require("@/assets/img2.jpg"),
  require("@/assets/img3.jpg")
];
//定义icon数组
const iconArr = [
  { icon: "gem-o", txt: "数码" },
  { icon: "gift-o", txt: "图书" },
  { icon: "music-o", txt: "日用" },
  { icon: "video-o", txt: "生鲜" },
  { icon: "refund-o", txt: "宠物" },
  { icon: "new-o", txt: "阿龙" },
  { icon: "good-job-o", txt: "阿坤" },
  { icon: "alipay", txt: "物流" }
];
export default {
  name: "home",
  components: {
    ZNav,
    ZGoods
  },
  data() {
    return {
      imgArr,
      iconArr
    };
  }
};
</script>

<style lang="scss" scoped>
.home {
  .swipe {
    .swipe-item {
      overflow: hidden;
      img {
        width: 375px;
        height: 190px;
      }
    }
  }
  .grid {
    // margin-top: 2px;
  }
}
</style>