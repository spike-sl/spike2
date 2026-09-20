<template>
  <!-- v-bind可省略，前面只加个： -->
  <div v-bind:class="class">绿龙</div>
  <div v-bind:id="id">肥美</div>

  <button :disabled="case">确定</button>
  
  <div v-bind="object">猎鹰</div>
</template>

<script>
  export default {
    data() {
      return{
        class:"spirit",
        id:"faze",
        // case:false
        case:true,

        object:{
          id:"niko",
          class:"monesy"
        }
            }
    }
  }
</script>