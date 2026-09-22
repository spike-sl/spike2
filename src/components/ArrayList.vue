<template>
    <h3>数组变化侦听</h3>
    <button @click="addList">添加</button>

    <ul>
        <li v-for="(item,index) of name" :key="index">{{ item }}</li>
    </ul>

    <button @click="together">合并</button>
    <h3>数组一</h3>
    <p v-for="(item,index) of num1" :key="index">{{ item }}</p>
    <h2>数组二</h2>
    <p v-for="(item,index) of num2" :key="index">{{ item }}</p>
</template>


<script>
    export default {
        data() {
            return{
                name:["donk","niko","zmjjkk"],
                num1:[1,2,3,4,5],
                num2:[6,7,8,9,10]
            }
        },
        methods:{
                addList(){
                    // ui自动变化
                    // this.name.push("smoggy")
                    this.name = this.name.concat(["smoggy"])
                },
                together(){
                    this.num1 = this.num1.concat(this.num2)
                }
            }
    }
</script>