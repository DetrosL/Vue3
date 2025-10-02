<script setup>
    import { ref } from 'vue'
    
    const title_todo = ref('')
    const completed = ref(false)
    
    function addTodo() {
      console.log('teste1', title_todo.value, completed.value)
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
