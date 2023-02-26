<template>
  <div class="container">
    <Category title="美食">
      <img
        slot="center"
        src="https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.91huoke.com%2Fxxfl%2Fhk91%2Fcustomer%2F48015%2FT3HsX2zsp1WUkggUyAR19CSGC9gFsU0JSmUiOxxy.jpeg&refer=http%3A%2F%2Fimg.91huoke.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1664027417&t=9ef5a1e9fd09db856afa2f85d6030b79"
        alt=""
      />
      <a slot="footer" href="http://baidu.com/">更多美食</a>
    </Category>

    <Category title="游戏">
      <ul slot="center">
        <li v-for="(g, index) in games" :key="index">{{ g }}</li>
      </ul>
      <div class="foot" slot="footer">
        <a slot="footer" href="http://baidu.com/">单机游戏</a>
        <a slot="footer" href="http://baidu.com/">网络游戏</a>
      </div>
    </Category>

    <Category title="电影">
      <video
        slot="center"
        controls
        src="http://www.w3school.com.cn/example/html5/mov_bbb.mp4"
      ></video>
      <template v-slot:footer>
      <div class="foot" >
        <a href="http://baidu.com/">经典</a>
        <a href="http://baidu.com/">推荐</a>
        <a href="http://baidu.com/">热门</a>
      </div>
      <h4>欢迎前来观影</h4>
      </template>

    </Category>
  </div>
</template>

<script>
import Category from "./components/Category.vue";
export default {
  name: "App",
  components: { Category },
  data() {
    return {
      foods: ["火锅", "烧烤", "小龙虾", "牛排"],
      games: ["红色警戒", "穿越火线", "劲舞团", "超级玛丽"],
      films: ["《教父》", "《拆弹专家》", "《你好，李焕英》", "《尚硅谷》"],
    };
  },
};
</script>

<style scoped>
.container,
.foot {
  display: flex;
  justify-content: space-around;
}

h3 {
  text-align: center;
  background-color: orange;
}

img {
  width: 100%;
}
video {
  width: 100%;
}
h4{
  text-align:center;
}
</style>
