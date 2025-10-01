<template>
    <div>

    <h2 :class=" { 'title': true, 'home-title': isHome } ">
        Vue 3
    </h2>

    <p :class="pClass">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum
    </p>

    <p :class="['text', { 'text-home': isHome }]">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum
    </p>

        <div 
            v-for="obj in todos"
            :key="obj.id"    
            class="todos-item"
        >
            <img
                v-if="obj.imgSrc"
                :src="obj.imgSrc"
            >
            {{ obj.title }}
        </div>

    </div>
</template>
<script>
    export default {
        name: 'App',
        data(){
            return {
                isHome: true,
                pClass: ['text', 'text-home'],
                todos: [
                    {
                        "userId": 1,
                        "id": 1,
                        "title": "delectus aut autem",
                        "completed": false,
                        "imgSrc": 'https://placehold.co/150' 
                    },
                    {
                        "userId": 1,
                        "id": 2,
                        "title": "quis ut nam facilis et officia qui",
                        "completed": false
                    },
                    {
                        "userId": 1,
                        "id": 3,
                        "title": "fugiat veniam minus",
                        "completed": false,
                        "imgSrc":'https://placehold.co/150'
                    },
                    {
                        "userId": 1,
                        "id": 4,
                        "title": "et porro tempora",
                        "completed": true
                    },
                    {
                        "userId": 1,
                        "id": 5,
                        "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
                        "completed": false
                    }
                ]
            }
        }
    }
</script>
<style>
    .title {
        font-size: 20px;
        color: blue;
    }

    .home-title {
        font-size: 40px;
        color: green;
    }

    .text {
        color: red;
    }

    .text-home {
        color: #42b983;
    }

    .todos-item {
        background: #000;
        margin: 0 0 5px 0;
        padding: 3px 6px;
        color: #fff;
    }
    
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        color: #2c3e50;
        margin: 60px;
    }
</style>