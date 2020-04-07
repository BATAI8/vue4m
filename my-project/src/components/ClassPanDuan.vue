<template>
  <!-- class的判断与使用 -->
  <div>
    <!-- 对象 -->
    <p :class="{ t1: text }">213123</p>
    <!-- 数组里面传对象 -->
    <p class="t1" :class="[t22]">213123</p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      text: true,
      t22: {
        t2: true
      }
    };
  }
};
</script>

<style lang="less">
.t1 {
  background: red;
}
.t2 {
  color: yellow;
}
</style>
