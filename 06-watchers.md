## watchers
```html
    <div>
        <input 
            v-model="name"
            type="text"
        >
    </div>
```
#### as soon as I change this input, I want to save it to the database/run a secondary action.
```js
    export default {
        name: 'App',
        data() {
            return {
                name: '';
            }
        },

        watch: {
            name(newValue, oldValue) { 
                console.log(newValue, oldValue);
                if(newValue.length >= 4){
                    this.saveUserName()
                }
            }
        }

        methods: {
            saveUserName() {
                console.log(this.name);
            }
        }
    }
```
#### another example:
```html
    <div>
        <select v-model="pageCount">
            <option value="5">5</option>
            <option value="10">10</option>
            <option value="15">15</option>
        </select> <br>
        {{ pageCount }}
    </div>
```
#### as soon as I change this input, I want to save it to the database/run a secondary action.
```js
    export default {
        name: 'App',
        data() {
            return {
                pageCount: 5,
            }
        },

        watch: {
            pageCount() {
                this.changePage();
            },
        }

        methods: {
            changePage() {
                console.log('Ajax changePage');
            }
        }
    }
```