<template>
    <div class="outer">
        <h4>v-for 与 父子传值</h4>
        
        <VFChild 
            v-for="item of items" 
            :item="item"
            :key="item.id"
        />

        <!-- <div v-for="numbers in sets">
            <p v-for="n in even(numbers)">{{ n }}</p>
        </div> -->
    </div>
</template>

<script setup>
    import VFChild from '../CompositionApi/VForChild.vue';
    import {ref,reactive} from 'vue';
    const items = ref([
        {id:1,name:"bruce"},
        {id:2,name:"nico"},
        {id:3,name:"xiaobai"},
        {id:4,name:"xiaohua"},
        {id:5,name:"nuomi"}
    ])

    // const sets = ref([
    //     [1, 2, 3, 4, 5],
    //     [6, 7, 8, 9, 10]
    // ])

    // function even(numbers) {
    //     return numbers.filter((number) => number % 2 === 0)
    // }
    
</script>

<style>
    
</style>