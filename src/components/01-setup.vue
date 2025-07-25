<script setup>
// setup
// 1.执行时机，比beforeCreate早
// 2.setup函数中获取不到this（此时this为underfined）
// 3.数据和函数，需要return才能在模板中使用
// 4.可以通过setup语法糖简化代码
// export default {
  // setup() {
  //   console.log('setup执行了');
  //   // 数据
  //   const datas = 'hello vue3'
  //   // 函数
  //   const fun = () => {
  //     console.log(datas);
  //   }
  //   return {  
  //     datas,
  //     fun
  //   }
    
  // },
//   beforeCreate(){
//     console.log("beforeCreate执行了");
//   }
// }
// 数据
 const datas = 'hello vue3'
// 函数
  const fun = () => {
    console.log(datas);
  }
</script>
<template>
<div>{{ datas }}</div>
<button style=" border: 1px solid white;" @click="fun"></button>
</template>
