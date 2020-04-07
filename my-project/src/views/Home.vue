<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <home2></home2>
    <TodoVue></TodoVue>
    <ClassPanDuan />
    <InputText />
    <ZuJian :text1="text" />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import Home2 from "@/components/Home2.vue";
import TodoVue from "@/components/TodoVue.vue";
import ClassPanDuan from "@/components/ClassPanDuan.vue";
// 表单练习
import InputText from "@/components/InputText.vue";
// 组件传值
import ZuJian from "@/components/ZuJian.vue";
export default {
  name: "Home",
  data() {
    return {
      text: 123123123
    };
  },
  components: {
    // HelloWorld,
    Home2,
    TodoVue,
    ClassPanDuan,
    InputText,
    ZuJian
  }
};
</script>
