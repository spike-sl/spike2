<template>
    <h3>列表渲染</h3>
    <!-- item可替换成name或其他,in也可以用of代替 -->
    <p v-for="(item,index) in names">{{ item }}:{{ index }}</p>

    <div v-for="item in result">
        <p>{{ item.title }}</p>
        <img v-bind:src="item.awator" alt="">
    </div>

    <div>
        <!-- <p v-for="item of cases">{{ item }}</p> -->
        <p v-for="(value,key,index) of cases">{{ value }}-{{ key }}-{{ index }}</p>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                names:["张宁","石乐怡","赖静雪"],
                result:[
                    {
                        "id":2,
                        "title":"ryx",
                        "text":"石浦",
                        "awator":"",
                    },
                    {
                        "id":5,
                        "title":"sly",
                        "text":"丹城",
                        "awator":"",
                    },
                    {
                        "id":20,
                        "title":"ljx",
                        "text":"西周",
                        "awator":"",
                    },
                ],
                cases:{
                        name:"张宁",
                        age:20,
                        sex:"男"
                    }
                    

            }
        }
    }
</script>