<template>
    <h3>事件修饰符</h3>
    <a  @click.prevent="skip" href="https://www.2345.com/baidu/baidusearch.html">百度</a>

    <div @click="a">
        <p @click.stop="b">事件冒泡</p>
    </div>

</template>

<script>
    export default {
        data(){
            return {

            }
        },

        methods: {
            skip(e) {
                // e.preventDefault();
                console.log("点击");
            },

            a() {
                console.log(111)
            },

            b(e) {
                // e.stopPropagation();
                console.log(222);
                
            }
        }
    }
</script>