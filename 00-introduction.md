## What Vue is?
it's a toolbox to make development easier
- a JS framework for building interfaces — progressive, reactive, and component-based
    - **progressive:** adaptable to other frameworks and libraries
    - **reactive:** whenever something changes, the view updates automatically in the whole app
- in the MVC structure, Vue is mainly focused on the View layer
- main characteristics:
    - single file components (SFCs):
        - templates, scripts and style are in the same file, separated by blocks
    - directives (like in JS):
        - conditions and loops, binding, two-way data binding, events, watchers, etc.
    - ecosystem
        - vue devtools - browser
        - vue CLI
        - vue Router
        - vueX

## How it can be used?
#### example:
```js
    // declaration
    import { createApp, ref } from 'vue'

    createApp({
    setup() {
        return {
        count: ref(0)
        }
    }
    }).mount('#app')
```
```html
    <!-- use -->
    <div id="app">
    <button @click="count++">
        Count is: {{ count }}
    </button>
    </div>
```
**result:** a button that increments the counter by 1 each time you click it

#### if you want to add more actions, you just create functions inside `setup()` like this:
```js
    import { createApp, ref } from 'vue'

    createApp({
    setup() {
        const count = ref(0)

        function reset() {
        count.value = 0
        }

        function double() {
        count.value = count.value * 2
        }

        return {
        count,
        reset,
        double
        }
    }
    }).mount('#app')

```
#### and to use them, just put `#app` on a `<div>` and attach the functions to buttons:
```html
    <div id="app">
        <p>Count is: {{ count }}</p>
        <button @click="count++">+1</button>
        <button @click="double">Double</button>
        <button @click="reset">Reset</button>
    </div>
```
