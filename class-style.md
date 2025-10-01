## Class and Style
they can be bound to Vue with `v-bind`, allowing classes to recalculate themselves dynamically.
```
    <h2 :class=" { 'title': true, 'home-title': isHome } ">
```
- always applies `title`. If `isHome` is true, it also adds `home-title`.
```
    <p :class="['text', { 'text-home': isHome }]">
```
- apply an array of classes: use `text` as the base, and if `isHome` is true, add the class `text-home`.  
