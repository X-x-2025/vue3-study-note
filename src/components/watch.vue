<script setup>
// watch函数
// 作用：侦听一个或多个数据的变化，数据变化时执行回调函数
// 两个额外参数：
// 1.immediate（立即执行）
// 2.deep（深度侦听）

// 导入watch函数
import { ref , watch } from 'vue';
// 调用watch，侦听变化
// 侦听单个数据
// watch(要侦听的数据,(newValue,oldValue) => {
//   console.log(`数据发生了变化,新值为${newValue}，老值为${oldValue}`); 
// })
// 侦听多个数据
// watch([要侦听的数据1,要侦听的数据2],([newValue,oldValue],[newValue,oldValue]) => {
//   console.log('数据发生了变化',[newValue,oldValue],[newValue,oldValue]); 
// })
// const name = ref('张三');
// const age = ref(18);
// const changeName = () => {
//   name.value = '李四'
// }
// const changeAge = () => {
//   age.value++
// }
// 侦听单个数据
// watch(age,(newAge,oldAge) =>{
//   console.log(newAge,oldAge)
// })
// 侦听多个数据
// watch([name,age],([newName,oldName],[newAge,oldAge]) =>{
//   console.log([newName,oldName],[newAge,oldAge]);
// })

// 参数immediate
// 作用：在侦听函数创建时立即触发回调，响应式数据变化之后继续执行回调
// watch(age,(newAge,oldAge) =>{
//   console.log(newAge,oldAge)
// },{immediate:true})

// 参数deep
// 作用：深度监视，watch默认是浅层监视
// 例如：
// const ref1 = ref(简单类型)  可以直接监视
// const ref2 = ref(复杂类型)  监视不到复杂类型内部数据的变化
const obj = ref({
  name:'王五',
  age:18

})
const changeAge = () => {
  obj.value.age++
}
// 侦听整个对象
// watch(obj,(newValue) => {
//   console.log(newValue);
// },{deep:true})

// 侦听内部某个属性
watch(() => obj.value.age,(newAge,oldAge) => {
  console.log(newAge,oldAge);
},{deep:true})


</script>

<template>
  <!-- <div>{{ name }}</div>
  <button @click="changeName">改名字</button>
  <div>{{ age }}</div>
  <button @click="changeAge">改年龄</button> -->
  <div>-------------------</div>
  <h3>复杂类型的监视</h3>
  <div>{{ obj }}</div>
  <button @click="changeAge">增加年龄</button>

</template>