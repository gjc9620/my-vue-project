
<template>
  <div class='a1111'>
    <div>1111</div>
    <div>{{ 1111 }}</div>
    <!--<div>{{ (()=>{-->
       <!--debugger-->
      <!--})() }}</div>-->
    <div class='c1'>{{ data.aa }}</div>
    <div>222</div>
  </div>
</template>

<script>
  export default {
    components: {
      // BaseInputText, TodoListItem
    },
    data () {
      // debugger
      return {
        data: {
          type: Object,
          required: true,
          aa: this.$attrs.data.aa,
        }
      }
    },
    methods: {}
  }
</script>
