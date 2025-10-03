<script setup>
    import { inject, ref } from 'vue'
    import TodoForm from './TodoForm.vue'
    import TodoItem from './TodoItem.vue'

    const list_todo = inject('list_todo');
    const add = ref(false);

    function handleDeleteTodo(todo) {
        list_todo.value = list_todo.value.filter(t => t.id !== todo.id)
    }

    function openAdd() {
        add.value = true;
    }
</script>
<template>
  <div class="lista">
    <button type="button" @click="openAdd">ADD</button>
     
    <TodoForm v-if="add.value"/>
    <h1>Lista de todos</h1>
    <div v-for="todo in list_todo" :key="todo.id">
        <TodoItem :todo="todo" @delete-todo="handleDeleteTodo" />
    </div>
  </div>
</template>
