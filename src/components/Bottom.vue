<script setup>
import { inject } from 'vue';

 const topdata = inject('data')
 const topdata1 = inject('data1')
 const changeCount = inject('changeCount')
 const clickfn = () => {
   changeCount()
 }
</script>

<template>
  <h4>我是底层组件----{{ topdata }}----{{ topdata1 }}</h4>
  <button @click="clickfn">count自加</button>



</template>