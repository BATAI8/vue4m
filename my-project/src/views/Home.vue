<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <home2></home2>
    <TodoVue></TodoVue>
    <ClassPanDuan />
    <InputText />

    <!-- 父传子的写法 -->
    <ZuJian :text1="text" />

    <!-- 子传父的写法 -->
    <ZUJianzcf @text="getz" />
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
// 父传子组件传值
import ZuJian from "@/components/ZuJian.vue";

// 子传父组件传值
import ZUJianzcf from "@/components/ZUJianzcf.vue";
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
    ZuJian,
    ZUJianzcf
  },
  methods: {
    getz: function(t) {
      console.log(t);
    }
  }
};
</script>
