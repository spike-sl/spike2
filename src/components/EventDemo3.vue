<template>
    <h3>事件传参</h3>
    <div @click="add(item,$event)" v-for="(item,index) of names" :key="index">{{ item }}</div>
</template>

<script>
    export default{
        data(){
            return {
                names:["niko","donk","device"]
            }
            
        },
        methods: {
                add(name,e){
                    console.log(name);
                    console.log(e);

                }
            }
    }
</script>