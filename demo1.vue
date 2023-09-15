<script>
import { ref, computed } from 'vue';
// 声明数据
const list =ref ([1,2,3,4,5,6])

// 派生计算属性

const computedList = computed(()=>{
    return list.value.filter(item => item>=2)
})

// 定义一个修改数组的方法


</script>


<template>
    <div>{{ list }}</div>
    <div>{{ computedList }}</div>
</template>