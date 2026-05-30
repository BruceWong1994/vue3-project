<template>
    <p>{{ item.id }}: {{ item.name }}</p>
</template>

<script setup>
    //Vue2 或 Vue3选项式的写法
//    export default{
//         props:["item"]
//    } 

   //Vue3的组合式写法
//    const props = 
   defineProps(["item"])
//    console.log(props)
</script>

<style>
    
</style>