<template>
  <div>
    <!-- 多选 -->
    <input type="checkbox" v-model="checkbox1" value="a" />a
    <input type="checkbox" v-model="checkbox1" value="b" />b
    <input type="checkbox" v-model="checkbox1" value="c" />
    <!-- 直接就可以获取到值 -->
    {{ checkbox1 }}

    <!-- 单选 -->
    <p><input type="radio" value="男" v-model="ra" />男</p>
    <p><input type="radio" value="女" v-model="ra" />女</p>
    {{ ra }}
  </div>
</template>
<script>
export default {
  data() {
    return {
      checkbox1: [],
      ra: ""
    };
  }
  // methods: {
  //   ft: function() {
  //     console.log(this.checkbox1);
  //   }
  // }
};
</script>
<style lang="less" scoped></style>
