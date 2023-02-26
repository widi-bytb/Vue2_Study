<template>
  <div>
    <button @click="isShow = !isShow">显示/隐藏</button>
    <transition name="animation" appear>
      <h1 v-show="isShow">你好啊！</h1>
    </transition>
  </div>
</template>

<script>
export default {
  name: "Test2",
  data() {
    return {
      isShow: true,
    };
  },
};
</script>

<style scoped>
h1 {
  background-color: orange;
}

/* 进入的起点,离开的终点 */
.animation-enter,
.animation-leave-to {
  transform: translateX(-100%);
}
.animation-enter-active,
.animation-leave-active {
  transition: 1s linear;
}
/* 进入的终点,离开的起点 */
.animation-enter-to,
.animation-leave {
  transform: translateX(0);
}
</style>>

</style>