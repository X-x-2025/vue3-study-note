<script setup>
import Center from './components/Center.vue';
import { ref,provide } from 'vue';
// provide和inject
// 应用场景：顶层组件向任意的底层组件传递数据和方法，实现跨层组件通信
// 1.顶层组件通过provide函数提供数据
// 2.底层组件通过inject函数获取数据

// 1.跨层级传递普通数据
provide('data','我是顶层组件传递的数据')
// 2.跨层级传递响应式数据
const count = ref(100)
provide('data1' , count)
// 3.跨层级传递函数 可以让底层组件修改数据
provide('changeCount',() => {
  count.value++
})
</script>

<template>
  <h2>我是顶层组件</h2>
  <Center></Center>
</template>