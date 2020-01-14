<template>
  <div id="app">
    <!-- <TodoList></TodoList> OR <TodoList/> -->
    <b-container>
      <b-row>
        <b-col><TodoList/></b-col>
      </b-row>
    </b-container>
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
