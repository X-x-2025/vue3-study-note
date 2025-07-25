<script setup>
import { onMounted } from 'vue';
// Vue3的生命周期API
// 1.setup
// 2.onBeforeMount
// 3.onMounter
// 4.onBeforeUpdate
// 5.onUpdated
// 6.onBeforeUnmount
// 7.onUnmounted
const fun = () => {
  console.log('获取数据');
}
fun()
// 写成函数调用的方式，可以调用多次，并不会冲突，而是按照顺序依次执行
onMounted(() => {
  console.log('组件1挂载完成-----逻辑1');
})
onMounted(() => {
  console.log('组件2挂载完成-----逻辑2');
})
// 执行顺序：
// setup执行 → 创建响应式上下文 → 挂载DOM → 触发onMounted回调
// setup阶段（同步）
// ├─ 执行所有同步代码
// ├─ 注册onMounted回调
// └─ 结束
// ↓
// 挂载阶段（异步）
// └─ 触发已注册的onMounted回调

</script>

<template>
  
</template>