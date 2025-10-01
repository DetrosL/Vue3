<template>
    <div>
        <button @click="onClick" class="button">
            Send
        </button>
        <br><br>
        <div @mouseover.once="onMouseOver"
             @mouseout="onMouseOut">
            Mouse Over/Out
        </div>
        <br><br>
        <form action="https://google.com" @submit.prevent="onSubmit">
            <input type="text" @keyup="onKeyUp" class="input" placeholder="without modifiers"><br><br>
            <input type="text" @keyup.enter="onKeyUp" class="input" placeholder="with modifiers"><br><br>
            <button type="submit"
                class="button"
            >
                Enter
            </button>
        </form>
    </div>
</template>
<script>
    export default {
        name: 'App',
        data(){
            return {
                
            }
        },

        methods: {
            onClick($evt){console.log('click',$evt);},
            onMouseOver($evt){console.log('mouse over', $evt);},
            onMouseOut($evt){console.log('mouse out', $evt);},
            onSubmit($evt){console.log('submit', $evt);},
            onKeyUp($evt){console.log('onkeyup', $evt);},
        }
    }
</script>
<style>
    * {
        background-color: #2c3e50;
        color: #f7fbff;
        text-align: center;
    }

    .button {
        background-color: #880808; 
        color: white; 
        padding: 10px 20px; 
        border: none;
        border-radius: 5px;
        cursor: pointer;
        font-size: 16px;
        transition: background-color 0.3s ease;
    }

    .input {
        border: 1px solid #ccc; 
        padding: 8px;
        border-radius: 4px;
        font-size: 12px;
        width: 200px;
    }

    .button:hover {
        background-color: #671212;
    }

    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        color: #2c3e50;
        margin: 60px;
    }
</style>