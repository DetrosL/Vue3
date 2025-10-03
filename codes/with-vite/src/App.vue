<script setup>
    import TheHeader from './components/TheHeader.vue'
    import TodoForm from './components/TodoForm.vue'
    import TodoItem from './components/TodoItem.vue'
    import TodoList from './components/TodoList.vue'
    import { ref, provide } from 'vue'

    const list_todo = ref([]);
    provide('list_todo', list_todo);
</script>
<template>
    <div>
        <TheHeader />
        <TodoList />
    </div>
</template>
<style scoped>
    h1 {
        color: aliceblue;
    }
</style>
