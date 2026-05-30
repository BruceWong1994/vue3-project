<template>
    <div class="outer">
        <h4>计算属性</h4>
        <div>{{ age }}</div>
        <div>{{  fullName }}</div>
        <button @click="setNewValue">改名字</button>
    </div>
</template>

<script setup>
    import {ref,computed} from 'vue';

    const age = computed(()=>{
        return 1+22
    })
    const firstName = ref('John')
    const lastName = ref('Doe')
    const fullName = computed({
        // getter
        get() {
            // return firstName.value + ' ' + lastName.value
            return `${firstName.value} ${lastName.value}`
        },
        // setter
        set(newValue) {
            // 注意：我们这里使用的是解构赋值语法
            [firstName.value, lastName.value] = newValue.split(' ')
        }
    })
    // console.log(fullName.value);

    const setNewValue = () => {
        fullName.value = 'Bruce Wang';
        // console.log(fullName.value);
        // console.log(firstName.value);
        // console.log(lastName.value);
    }
</script>

<style>

</style>