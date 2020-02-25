<template>
  <div class="hello">
    <!-- <h1>
      <a name="hello-world" href="#hello-world">HelloWorld</a>
    </h1>-->

    <!-- 1,2,4的使用方法 -->
    <!-- <child></child> -->

    <!--3. this.$slots的用法 -->
    <!-- <child>
      <h1 slot="childheader">childheader</h1>
      <h2 slot="childbody">childbody</h2>
      <h3 slot="childfooter">childfooter</h3>
    </child>-->

    <!-- 5.作用域插槽 -->
    <!-- <child>
      <template slot-scope="scoped">{{scoped.text}}</template>
    </child>-->

    <!-- 官网例子 -->
    <render :level="2">hello</render>
  </div>
</template>

<script>
import render from "./render";
import child from "./child";

export default {
  components: { render, child },

  name: "HelloWorld",
  props: {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
