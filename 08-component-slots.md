## components slot
`v-slot:name`
* slots allow a base component to have a placeholder where the parent component (the one using the base) can insert custom content.
* in the base component, you use `<slot></slot>` to indicate where the content will appear.
* if the parent does not provide content for the slot, you can define default content inside the `<slot>` tag.

#### example 1:
```html
<!-- base -->
<button class="fancy-btn">
  <slot></slot>
</button>
```
```html
<!-- parent -->
<FancyButton>
  click me!
</FancyButton>
```
#### example 2:
```html
<!-- base -->
<header class="header">
  <h1>
    <slot name="title"/>
  </h1>
  <div>
    <slot name="description"/>
  </div>

  <div>
    <slot/>  
  </div>
</header>
```
```html
<!-- parent -->
<div>
  <Base>
    <template v-slot:title>
      home
    </template>

    <template v-slot:description>
      <p>i don't know</p>
    </template>

    header content - menu...
  </Base>
</div>
```
