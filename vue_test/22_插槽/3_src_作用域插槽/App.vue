<template>
  <div class="container">
    <Category title="游戏">
      <template scope="atguigu">
        <ul>
          <li v-for="(g, index) in atguigu.games" :key="index">{{ g }}</li>
        </ul>
      </template>
    </Category>
    

    <Category title="游戏">
      <template scope="{games}">
        <ol>
          <li v-for="(g, index) in games" :key="index">{{ g }}</li>
        </ol>
      </template>
    </Category>

    
    <Category title="游戏">
      <template slot-scope="{games}">
          <h4 v-for="(g, index) in games" :key="index">{{ g }}</h4>
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
     data() {
      return {
        
      }
     },
    }
  },
}
</script>

<style scoped>
.container {
  display: flex;
  justify-content: space-around;
}

img {
  width: 100%;
}
video {
  width: 100%;
}
h4 {
  text-align: center;
}
</style>
