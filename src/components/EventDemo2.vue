<template>
    <h3>内联与方法事件处理器</h3>
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
                add(e){
                    e.target.innerHTML = "增加" + this.count
                    this.count++
                }
            }
    }
</script>