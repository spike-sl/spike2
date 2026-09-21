<template>
    <h3>内联与方法事件处理器</h3>
    <p>{{ count }}</p>
    <!-- v-on:可以用@代替 -->
    <button v-on:click="count++">add</button>

    <p>{{ count }}</p>
    <button @click="add">增加</button>
</template>

<script>
    export default{
        data(){
            return {
                count:0
            }
            
        },
        methods: {
                add(){
                    this.count++
                }
            }
    }
</script>