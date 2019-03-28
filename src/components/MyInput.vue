<template>
  <div>
    <div>I am Input1 {{ searchText }}</div>
    <input
      v-bind:value=searchText
      v-on:input=onChange($event)
      />
<!--    <Input2 :modal=searchText :searchText=searchText />-->
  </div>
</template>

<script>
  import Input from './MyInput2';

  export default {
    components:{
      Input2: Input,
    },
    props: {
      searchText: {
        type: String,
        required: false
      },
      changeSearchText: {
        type: Function,
        required: false
      },
    },
    methods: {
      onChange($event){
        this.$emit('input', $event.target.value);
      }
    },
    data(){
      return {
        searchText: this.$attrs.searchText ,
      }
    },
  };
</script>
