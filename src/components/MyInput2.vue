<template>
  <div>
    <div>I am Input2 {{ searchText }}</div>
    <input
      v-bind:value=searchText
      v-on:input=onChange
      />
  </div>
</template>

<script>
  export default {
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
    // data(){
    //   return {
    //     searchText: ,
    //   }
    // },
  };
</script>
