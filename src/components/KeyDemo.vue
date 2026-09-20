<template>
    <h2>key属性添加</h2>

    <!-- 尽量使用id作为key的数据而不是index，这是为了确保key的唯一不变性 -->
    <div>
        <p v-for="(item,index) of names" :key="index">{{ item }}</p>
    </div>

    <div v-for="item of result" :key="item.id">
        <p>{{ item.title }}</p>
    </div>
</template>

<script>
    export default{
        data() {
            return {
                names:["spirit","faze","tyloo"],

                result:[
                {  
                    "id":1,
                    "title":"spitit",
                    "NOone":"donk",
                },
                {  
                    "id":10,
                    "title":"navi",
                    "NOone":"bit",
                },{  
                    "id":20,
                    "title":"faze",
                    "NOone":"fozen",
                },
            ]
            }
        }
    }
</script>