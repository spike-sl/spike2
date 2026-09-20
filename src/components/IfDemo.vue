<template>
    <h2>条件渲染</h2>
    <div v-if="flag">你能看见我吗</div>
    <div v-else>你会看到这条</div>

    <div v-if="type === 'A'">a</div>
    <div v-else-if="type === 'B'">b</div>
    <div v-else-if="type === 'C'">c</div>
    <div v-else>Not a/b/c</div>

    <div v-show="flag">这条也能看见</div>
</template>

<script>
    export default {
        data() {
            return {
                flag:true,
                // flag:false,
                type:"D"
            }
        }
    }

</script>