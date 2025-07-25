<script setup>
// 父传子
// 1.给子组件添加属性的方式传值
// 2.在子组件通过props接收

// 子传父
// 1.在子组件内部，emit触发事件
// 2.在父组件通过@监听
import { ref } from 'vue';
// 局部导入子组件
import SonComonent from './components/SonComonent.vue';
// 定义响应式数据
const money = ref(1000000)
const makeMoney = () => {
  money.value += 10000
}
const changeMoneyfn = (costvalue) => {
  money.value -= costvalue
}

</script>

<template>
  <div>
    <h2>父组件资产{{ money }}
      <!-- 动态控制 -->
      <button style="border: 1px solid white;" @click="makeMoney">挣钱</button>
    </h2>
    <!-- 给子组件添加属性的方式传值 -->
    <SonComonent 
    car="宝马" 
    :money="money"
    @changeMoney="changeMoneyfn"
    ></SonComonent>
  </div>
</template>