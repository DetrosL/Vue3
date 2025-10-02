## events
#### clicks, key presses… actions/interactions with the front-end
`v-on`: or shorthand `@`

#### example:
```html
    <button @click="onClick" class="button">
        Send
    </button>
    <br><br>
    <div @mouseover="onMouseOver"
        @mouseout="onMouseOut">
        Mouse Over/Out
    </div>
```
```js
    methods: {
        onClick($evt){console.log('click',$evt);},
        onMouseOver($evt){console.log('mouse over', $evt);},
        onMouseOut($evt){console.log('mouse out', $evt);},
	}
```

#### event modifiers
`.stop`, `.prevent`, `.self`, `.capture`, `.once`, `.passive`

#### examples:
```html
    <!-- the click event's propagation will be stopped -->
    <a @click.stop="doThis"></a>

    <!-- the submit event will no longer reload the page -->
    <form @submit.prevent="onSubmit"></form>

    <!-- only trigger handler if event.target is the element itself -->
    <div @click.self="doThat">...</div>
```
`.capture`, `.once` and `.passive` modifiers mirror the options of the native addEventListener method:
```html
    <!-- use capture mode when adding the event listener     -->
    <div @click.capture="doThis">...</div>

    <!-- the click event will be triggered at most once -->
    <a @click.once="doThis"></a>

    <!-- the scroll event's default behavior (scrolling) will happen immediately, instead of waiting for `onScroll` to complete  -->
    <div @scroll.passive="onScroll">...</div>
```

See the [Vue.js guide]('https://vuejs.org/guide/essentials/event-handling.html#event-modifiers') for more details.
