<template>
  <div>
    <div>
      <input type="text" v-model="keytext" v-on:keyup.enter="keys" />
    </div>

    <!-- // eslint-disable-next-line vue/require-v-for-key -->
    <ul v-for="(item, index) of list" :key="index">
      <li>{{ item }} <span v-on:click="remove">删除</span></li>
    </ul>

    <!-- 过滤器的使用 -->
    <p><span>性别：</span>{{ gender | fg }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      keytext: "",
      list: [],
      gender: 0
    };
  },
  methods: {
    keys: function() {
      console.log(this.keytext);
      this.list.push(this.keytext);
      this.keytext = "";
    },
    remove: function(index) {
      this.list.splice(index, 1);
    }
  },
  // 过滤器
  filters: {
    fg: function(value) {
      switch (value) {
        case 1:
          return "女";
        case 0:
          return "男";

        default:
          return "其他";
      }
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less"></style>
