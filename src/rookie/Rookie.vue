<template>
  <div class='a1111'>
    <div>1111</div>
    <div>{{ 1111 }}</div>
    <!--<div>{{ (()=>{-->
       <!--debugger-->
      <!--})() }}</div>-->
    <div class='c1'>{{ data.aa }}</div>
    <div>{{ getMess }}</div>
    <input :value="inputValue" @click="alert" />
    <div v-bind:class="{ active: true }">test class</div>
  </div>
</template>

<script>
  const vm = {
    components: {
      // BaseInputText, TodoListItem
    },
    created(){
      // this.data.aa = 5555;
      // // return
      // window.setTimeout(()=>{
      //   // debugger
      //   this.data.aa = 666;
      // }, 3e3);
      // debugger
    },
    beforeUpdate(){
      console.log(this.inputValue);
    },
    computed: {
      getMess: function () {
        // `this` 指向 vm 实例
        return this.mess.split('').reverse().join('')
      }
    },
    data(){
      return {
        data: {
          aa: 123123
        },
        mess: 'aabbcc',
        inputValue: '333',
      }
    },
    methods: {},
  };
  window.vm = vm;
  export default vm
</script>
