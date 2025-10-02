## props
#### props are a way to pass data from a parent component to a child component.
#### they make components more reusable and configurable, since you can change their behavior or appearance depending on the props received.
#### in the example: variant changes the CSS class (for styling, like success, error, warning), and text could be used to change the message displayed.

```html
<!-- BaseAlert -->
<div :class="baseClass">
  Your form has been submitted successfully
</div>
```
```js
export default {
  props: ['variant', 'text'],
  computed: {
    baseClass() {
      return [
        'alert',
        this.variant ? `alert-${this.variant}` : ''
      ]
    }
  }
}
```
#### using
```html
<div>
  <BaseAlert
    :variant="variant"
    :text="text"
  >
</div>
```
```js
export default {
  name: 'App',
  components: { BaseAlert },
  data() {
    return {
      variant: 'success',
      text: 'Your form has been submitted'
    }
  }
}

```
### compared to slots:
- props are more useful for defining behavior and configuration of a component.
- slots are better when you want to customize the content of a component.