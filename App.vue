<script setup>
import { computed,ref } from 'vue';

const list =ref( [1,2,3,4,5,6,7,8] )

const computedlist = computed(() =>{

  return list.value.filter(item=> item>=2)
})

const added =() =>{
  list.value.push(123)
}
</script>

<template>
  <div>原来的数组  ，{{list}}</div>
  <div>修改后的数组  ，{{ computedlist }}</div>

  <button @click="added">+123</button>
</template>