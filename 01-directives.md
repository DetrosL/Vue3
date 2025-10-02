## DIRECTIVES
#### used inside components
`v-show`, `v-if`, `v-for`

#### example:
```html
    <!-- v-show... -->
    <TheHeader 
        v-show="showHeader"
    />
```
```html
<template>
    <!-- v-if... -->
    <div v-if="accessLevel === 'admin'">Admin</div>
    <div v-else-if="accessLevel === 'marketing'">Marketing</div>
    <div v-else>User</div>

    <!-- v-for -->
    <div 
        v-for="var_local in array"
        :key="var_local.id"
    >
        {{ var_local.title }}
    </div>
</template>
<script>
    export default {
        name: 'App',
        data(){
            return {
                isHome: true,
                pClass: 'text',
                todos: [...]
            }
        }
    }
</script>
```

- v-show-> toggles the element's display using CSS (`display: none / block`).
- v-if  -> if the condition is not true, the element is not even rendered in the DOM.
- v-for	-> make a loop, key is used to give a single identification to each elemento
- and `v-bind:` or its shorthand `:` is used to bind a HTML attribute to a Vue variable/expression.
