<template>
  <div id="app">
    <h1>My Todo App!</h1>
    <TodoList/>
    11
    <MyRookie :data="data" />
    22
    <span>Multiline message is:</span>
    <p style="white-space: pre-line;">{{ data.message }}</p>
    <br>
    <textarea v-model="data.message" placeholder="add multiple lines"></textarea>
    <MyInput
      v-model="searchText"
      :searchText="searchText"
      />
    <!--<MyInput
      :searchText=searchText
      :changeSearchText=changeSearchText
      />-->
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue';
import Rookie from './rookie/Rookie';
import MyInput from './components/MyInput';

export default {
  components: {
    TodoList,
    MyRookie: Rookie,
    MyInput: MyInput,
  },
  methods:{
    changeSearchText(event){
      this.searchText = event.target.value;
    },
    testSearchText(){
      debugger
    },
  },
  created(){
    this.data.aa = 5566;
    // return
    // window.setTimeout(function () {
    //   // debugger
    //   // this.data.aa = 555;
    // }, 500);
    // debugger
  },
  data(){
    return {
      data: {
        aa: 123123,
        message: '111',
      },
			searchText: '333',
    }
  }
}
</script>

<style lang="scss">
@import './variables.scss';

*, *::before, *::after {
  box-sizing: border-box;
}

#app {
  max-width: 400px;
  margin: 0 auto;
  line-height: 1.4;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: $vue-blue;
}

h1 {
  text-align: center;
}
</style>
