<script setup>
import { defineExpose } from 'vue'
// defineExposeExpose()
// 默认情况下在<script setup>语法糖下组件内部的属性和方法是不开放给父组件访问的
// 可以使用defineExpose()方法来指定哪些属性和方法是可以暴露给父组件访问
const count = 99

defineExpose({
    count

})
</script>
<template>
<div>测试组件</div>
<div>计数器{{ count }}</div>
</template>
<style>

</style>