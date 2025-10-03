<script setup>
import { inject } from 'vue'
import TodoItem from './TodoItem.vue'

const list_todo = inject('list_todo')
</script>

<template>
  <div>
    <div v-for="todo in list_todo" :key="todo.id" >
        <TodoItem :todo="todo"/>
    </div>
  </div>
</template>
