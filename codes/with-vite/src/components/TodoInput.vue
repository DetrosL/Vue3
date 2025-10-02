<script setup>
    var title_todo  = '';
    var completed   = false;

    function addTodo(){
        console.log('teste1');
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

            <button @click="addTodo"></button>
        </form>
    </div>
</template>
<style scoped>

</style>