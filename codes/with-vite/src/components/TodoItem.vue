<script setup>
    import { defineProps } from 'vue';

    const props = defineProps({
        todo: Object,
        required: true
    })

    const emit = defineEmits(['delete-todo']);

    function deleteTodo() {
        emit('delete-todo', props.todo)
    }
</script>
<template>
    <div v-if="props.todo" class="card">
        <div class="card1">
            <h3> {{ props.todo.titleD }} </h3>
            <p>Status: {{ props.todo.completed ? '✅ Done' : '❌ Pending' }}</p>
        </div>
        <div class="card2">
            <button type="button" @click="deleteTodo">❌</button>
        </div>
    </div>
</template>
<style scoped>
   .card {
        display: flex;
        justify-content: space-between;
        align-items: stretch;
        background-color: #1e1e1e;
        color: #f5f5f5;
        padding: 0;
        border-radius: 5px;
        box-shadow: 0 4px 8px rgba(0,0,0,0.3);
        max-width: 400px;
        margin: 10px auto;
        font-family: 'Arial', sans-serif;
        transition: transform 0.2s, box-shadow 0.2s;
        height: 70px;
    }	

    .card:hover {
        transform: translateY(-2px);
        box-shadow: 0 8px 16px rgba(0,0,0,0.5);
    }

    .card1 {
        flex: 1;
        padding: 10px 20px;
    }

    .card2 {
        height: 100%;
    }

    .card2 button {
        height: 100%;
        border: none;
        padding: 0 20px;
        font-size: 1.5em;
        background-color: #7a1515;
        color: #fff;
        cursor: pointer;
        transition: background 0.25s;
        border-top-right-radius: 5px;
        border-bottom-right-radius: 5px;
    }

    .card2 button:hover {
        background-color: #a72222;
    }

</style>