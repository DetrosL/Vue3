<template>
    <div>

        <div>
            Two-way data binding <br>
            v-model -> forms
        </div>

        <br><br>
        <div>
            <label>Name</label><br/>
            <input
                v-model="name"
                type="text"
                class="input"
            > <br>
            {{ name }}
        </div>

        <br><br>
        <div>
            <label for="">books</label><br>
            <select v-model="books">
                <option value="">Choose</option>
                <option value="tog">Throne of Glass</option>
                <option value="eta">An Ember in the Ashes</option>
                <option value="cc">Crescent City</option>
            </select> <br>
            {{ books }}
        </div>

        <br><br>
        <div>
            <label for="">newsletter</label> <br>
            <input
                v-model="newsletter" 
                type="radio"
                value="yes"
                > yes
            <input
                v-model="newsletter" 
                type="radio"
                value="no"
                > no <br>
            {{ newsletter }}
        </div>

        <br><br>
        <div>
            <label for="">contracts</label><br>
            <input 
                v-model="contract"
                type="checkbox"> accept our terms... <br>
            {{ contract }}
        </div>

        <br><br>
        <div>
            <label for="">select the colors you like</label><br>
            <input
                v-model="colors" 
                type="checkbox"
                value="red"
                > red
            <input
                v-model="colors" 
                type="checkbox"
                value="purple"
                > purple
            <input
                v-model="colors" 
                type="checkbox"
                value="black"
                > black
            <input
                v-model="colors" 
                type="checkbox"
                value="blue"
                > blue <br>
                {{ colors }}
        </div>

    </div>
</template>
<script>
    export default {
        name: 'App',
        data(){
            return {
                name: 'Daenerys Targaryen',
                books: 'tog',
                newsletter: 'yes',
                contract: false,
                colors: [],
            }
        }
    }
</script>
<style>
    * {
        background-color: #18232e;
        color: #FFF;
        text-align: center;
    }

    .input {
        border: 1px solid #ccc; 
        padding: 8px;
        border-radius: 4px;
        font-size: 12px;
        width: 200px;
    }

    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        margin: 60px;
    }
</style>