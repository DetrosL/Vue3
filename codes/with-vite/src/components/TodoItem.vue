<script setup>
    import { defineProps } from 'vue';

    const props = defineProps({
        todo: {
            type: Object,
            required: true
        }
    });
</script>
<template>
    <div class="card">
        <!-- <h3> {{ todo.title }} </h3> -->
         <h3>test</h3>
        <!-- <p>Status: {{ todo.completed ? '✅ Done' : '❌ Pending' }}</p> -->
         <p> stts</p>
    </div>
</template>
<style scoped>
    .card {
        background-color: #1e1e1e;
        color: #f5f5f5;
        padding: 20px;
        border-radius: 5px;
        box-shadow: 0 4px 8px rgba(0,0,0,0.3);
        max-width: 400px;
        margin: 10px auto;
        font-family: 'Arial', sans-serif;
        transition: transform 0.2s, box-shadow 0.2s;
    }

    .card:hover {
        transform: translateY(-5px);
        box-shadow: 0 8px 16px rgba(0,0,0,0.5);
    }

    .card p {
        margin: 0;
        font-size: 14px;
        color: #ccc;
    }
</style>