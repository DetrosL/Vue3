## computed progressions 
#### if instead you create a method/function instead, the data will be recomputed every time the component re-renders. <br> Using a computed property makes the value update only when its dependencies change, which is usually more efficient.

- **Computed** → only recalculates when the variables it depends on change.
- **Method** → runs every time the template re-renders, even if nothing has changed.

```html vue
<div> 
	{{ fullName }}
</div>
```
```js
export default {
	data() {
		return {
			user: {
				first_name: 'Daenerys',
				last_name: 'Targeryan'
			}
		}
	},
	
	computed: {
		fullName(){
			return `${this.user.first_name} ${this.user.last_name}`
		},
	}
	
}
```
#### more completed example:
```html
    <div>
        <h2>todos incomplete</h2>
        <div
            v-for="todo in incompleteTodos"
            :key="todo.id"
        >
            {{ todo.title }}
        </div>

        <h2>todos completed</h2>
        <div
            v-for="todo in completedTodos"
            :key="todo.id"
        >
            {{ todo.title }}
        </div>
        <br>
        <h2>To dos</h2>
        <div
            v-for="todo in todos"
            :key="todo.id"
        >
            <input
                v-model="todo.completed"
                type="checkbox"
            >
            {{ todo.title }}
        </div>

    </div>
```
```js
export default {
    name: 'App',
    data() {
        return {
            todos: [
                {
                    "userId": 1,
                    "id": 1,
                    "title": "delectus aut autem",
                    "completed": false
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
                    "completed": false
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
    },

    computed: {
        incompleteTodos() {
            return this.todos.filter(todo => !todo.completed);
        },
        completedTodos() {
            return this.todos.filter(todo => todo.completed)
        },
    },
}
```
