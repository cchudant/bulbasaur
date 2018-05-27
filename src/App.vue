<template>
  <div id="app">
    <p>My TodoList</p>
    <todo-list :todos="todos" @delete="onDelete"></todo-list>
    <todo-input @add="onAdd"></todo-input>
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue'
import TodoInput from './components/TodoInput.vue'

export default {
  name: 'app',
  components: {
    TodoList,
    TodoInput
  },
  data() {
    return {
      todos: ['learn Vue!']
    }
  },
  methods: {
    onAdd(todo) {
      this.todos.push(todo)
    },
    onDelete(i) {
      this.todos.splice(i, 1)
    }
  }
}
</script>
