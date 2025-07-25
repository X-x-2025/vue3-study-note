<script setup>
// 模板引用
// 概念：通过ref标识获取真实的dom对象或者组件实例对象
// 语法
import { ref } from 'vue';
// 1.调用ref函数生成一个ref对象
const h2Ref = ref(null)


</script>

<template>
  <!-- 2.通过ref标识绑定ref对象 -->
  <h2 ref="h2Ref"></h2>
  <div>
    <input type="text">
    <button>点击输入框聚焦</button>
  </div>
</template>