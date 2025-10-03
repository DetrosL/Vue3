<script setup>
    import { ref, inject } from 'vue'

    const list_todo     = inject('list_todo');
    const title_todo    = ref('');
    const completed     = ref('');
    
    function addTodo() {
        const lastId = list_todo.value.length > 0 ? list_todo.value[list_todo.value.length - 1].id : 0

        list_todo.value.push({
            id: lastId + 1,
            title: title_todo.value,
            completed: completed.value,
        })
    
        title_todo.value = '';
        completed.value = '';
    }
</script>
<template>
    <div>
        <form @submit.prevent="addTodo"> <!-- previne o recarregamento da página e chama sua função. -->
            <label>Title todo</label><br>
            <input 
                v-model="title_todo"
                type="text">
            <br>
            <label>Completed</label><br>
            <input 
                v-model="completed"
                type="radio"
                :value="true"> Yes
                
            <input 
                v-model="completed"
                type="radio"
                :value="false"> No

            <br><br>

           <button type="submit">Adicionar</button>
        </form>
    </div>
</template>
<style scoped>
    div {
        background-color: #3b3a3a;
        padding: 20px;
        max-width: 400px;
        margin: 0 auto;
        border-radius: 10px;
    }

    label {
        font-size: 20px;
    }

    input[type="text"]{
        width: 20em;
        padding: 0.6em;
        margin-bottom: 1em;
        border: 1px solid #ccc;
        border-radius: 5px;
        font-size: 16px;
        box-sizing: border-box;
    }

    input[type="radio"]{
        width: 1.5em;
        padding: 0.6em;
        border: 1px solid #ccc;
        font-size: 16px;
    }

    button {
        border-radius: 8px;
        border: 1px solid transparent;
        padding: 0.6em 1.2em;
        font-size: 1em;
        font-weight: 500;
        font-family: inherit;
        background-color: #1a1a1a;
        cursor: pointer;
        transition: border-color 0.25s;
    }
    button:hover {
        border-color: #646cff;
    }

</style>
