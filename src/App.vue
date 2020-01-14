<template>
  <div id="app">
    <TodoList></TodoList>
  </div>
</template>

<script>
import TodoList from './components/TodoList'

export default {
  name: 'app',
  components: {
    TodoList,
  }
}
</script>

<style>
#app {
  font-family: 'Raleway', sans-serif;
}
</style>
