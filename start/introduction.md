

## What Vue is?

it's a box of tools, 

## How it can be used?
#### example:
```
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
```
    <!-- use -->

    <div id="app">
    <button @click="count++">
        Count is: {{ count }}
    </button>
    </div>
```
**result:** a button that increments the counter by 1 each time you click it

#### if you want to add more actions, you just create functions inside `setup()` like this:
```
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
```
    <div id="app">
        <p>Count is: {{ count }}</p>
        <button @click="count++">+1</button>
        <button @click="double">Double</button>
        <button @click="reset">Reset</button>
    </div>
```