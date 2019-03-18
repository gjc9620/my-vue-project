<template>
	<div id="app">
		<h1>My Todo App!</h1>
		<TodoList/>
		11
		<MyRookie :data="data" />
		22
	</div>
</template>

<script>
import TodoList from './components/TodoList.vue'
import Rookie from './rookie/Rookie'

export default {
	components: {
		TodoList,
    MyRookie: Rookie,
	},
	data(){
	  return {
      data: {
        aa: 123123
			}
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
