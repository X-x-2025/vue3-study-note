<script setup>
// 借助“编译器宏”函数接收父组件传递过来的数据
const props = defineProps({
    car:String,
    money:Number
})
const emit = defineEmits(['changeMoney'])
const cost = () =>{
    // 需要emit触发事件
    // 触发'changeMoney'事件时通知父组件
    emit('changeMoney', 5000)
}
</script>

<template>
<div class="son">子组件继承了{{ car }}和{{ money }}
    <button @click="cost">花钱</button>
</div>

</template>

<style>
.son{
    padding: 10px;
    border: 1px solid white;
}
</style>