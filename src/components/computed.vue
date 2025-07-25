<script setup>
// computed计算属性函数
// 和vue2计算属性一致，但是vue2的计算属性是一个对象，vue3的计算属性是一个函数
// 步骤
// 1.导入computed
import { computed } from 'vue';
// 2.执行函数在回调参数中return基于响应式数据的计算的值，用变量接收
const sum = computed(()=>{
    return 计算之后的值

})
</script>