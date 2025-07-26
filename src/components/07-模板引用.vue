<script setup>
// 模板引用
// 概念：通过ref标识获取真实的dom对象或者组件实例对象
// 语法
import { ref } from 'vue';
import TextComponent from './components/TextComponent.vue'
import { onMounted } from 'vue'
// 1.调用ref函数生成一个ref对象
const input = ref(null)
const Text = ref(null)

onMounted(() => {
  console.log(input.value);
})
const clickfn  =() => {
  input.value.focus()
}
const getComponent = () => {
  console.log(Text.value.count);
  
}
</script>

<template>
  <!-- 2.通过ref标识绑定ref对象 -->
  <h2>标题</h2>
  <div>
    <input ref="input" type="text">
    <button @click="clickfn">点击输入框聚焦</button>
    <TextComponent ref="Text"></TextComponent>
    <button @click="getComponent">获取组件数字</button>
  </div>
</template>