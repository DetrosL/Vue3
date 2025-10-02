<script setup>
    import { ref } from 'vue'

    const list_todo = ref([])
    const title_todo = ref('')
    const completed = ref(false)
    
    function addTodo() {
        const lastId = list_todo.value.length > 0 
        ? list_todo.value[list_todo.value.length - 1].id 
        : 0

        list_todo.value.push({
            id: lastId + 1,
            title: title_todo.value,
            completed: completed.value,
        })
    
        title_todo.value = ''
        completed.value = false
    }
</script>
<template>
    <div>
        <form action="">
            <label for="">title todo</label><br>
            <input 
                v-model="title_todo"
                type="text">

            <br><br>

            <label for="">completed?</label><br>
            <input 
                v-model="completed"
                type="checkbox">

           <button type="button" @click="addTodo">Adicionar</button>
        </form>
    </div>
</template>
<style scoped>

</style>
