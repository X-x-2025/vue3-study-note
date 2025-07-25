<script setup>
// ref:接收简单类型或复杂类型，返回一个响应式的对象
// 1.接收简单类型，返回一个对象，对象.value就是接收的值
// 本质上是包成复杂类型，再借助reactive实现响应式
// 注意：1.在脚本中，访问数据时需要通过.value来访问
//      2.在template中，访问数据时不需要.value来访问
// 导入ref
import { ref } from 'vue';
const count = ref(666)
console.log(count.value);



</script>