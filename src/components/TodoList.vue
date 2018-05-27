<template>
  <ol>
    <li
      v-for="(todo, i) in todos"
      :key="todo"
      @click="$emit('delete', i)"
      class="todoItem"
    >
      {{todo}}
    </li>
  </ol>
</template>

<script>
export default {
  props: {
    todos: Array
  }
}
</script>

<style>
.todoItem:hover::after {
  content: ' [X]';
}
</style>
