<script setup>
    import { inject } from 'vue'
    import TodoItem from './TodoItem.vue'

    const list_todo = inject('list_todo');
</script>
<template>
  <div>
    <div v-for="todo in list_todo" :key="todo.id" >
        <TodoItem :titleD="todo.title" :completed="todo.completed" />
    </div>
  </div>
</template>
