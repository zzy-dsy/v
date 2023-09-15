<script>
// setup
// 执行时机比beforecreate还要早
// setup函数中获取不到this 
// 数据 和 函数，需要在 setup 最后return， 才能在模板中应用
</script>

<script setup>
// import { reactive } from 'vue';
// const state = reactive({
//   count: 100
// })
// const setCount = () =>{
//   state.count++
// }

import { ref } from 'vue';
const count =ref(0)
console.log(count.value)

const setCount = () =>{
  count.value++
}
</script>

<template>
  <div>{{ count }}</div>
  <button @click="setCount">+1</button>
</template>

<!-- <template>
  <div>{{ state.count }}</div>
  <button @click="setCount">+1</button>
</template> -->