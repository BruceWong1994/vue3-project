<template>
    <div>
        <p>my name is {{ name }}, i'm {{ age }} years old</p>
        <!-- <p>{{ info }}</p> -->
         <div><button @click="addHandler">count:{{ count }}</button></div>
         <div>这是第{{ count }}次点击</div>
    </div>
</template>

<script>
    //选项式api
    export default{
        data(){
            return {
                name:'Bruce',
                age: 31,
                count:0
            }
        },
        // computed(){
        //     return {
        //         info:`my real name is${this.name}, i'm ${this.age} years old already`
        //     }
            
        // },
        methods:{
            addHandler(){
                this.count ++
            }
        }
    }
</script>

<style>

</style>