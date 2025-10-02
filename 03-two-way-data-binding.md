## two-way data binding
#### vhen the view and the data are always synchronized automatically.
	**basically:** if you change the variable → the input changes too... and if you change the input → the variable changes.
- data ↔ interface

#### examples:
```html
	<div>
  		<label>name</label><br/>
  	<input v-model="name" type="text">
  	<br>
  	{{ name }}
	</div>
```
```html
	<div>
  		<label>books</label><br>
  		<select v-model="books">
    			<option value="">Choose</option>
    			<option value="tog">Throne of Glass</option>
    			<option value="eta">An Ember in the Ashes</option>
    			<option value="cc">Crescent City</option>
  		</select>
  		<br>
  		{{ books }}
	</div>
```
```html
    <div>
        <label for="">select the colors you like</label><br>
        <input
            v-model="colors" 
            type="checkbox"
            value="red"
        > red
        <input
            v-model="colors" 
            type="checkbox"
            value="purple"
        > purple
        <input
            v-model="colors" 
            type="checkbox"
            value="black"
        > black
        <input
            v-model="colors" 
            type="checkbox"
            value="blue"
            > blue <br>
           {{ colors }}
    </div>
```
