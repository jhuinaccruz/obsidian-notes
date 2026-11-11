# HTML 
## Buttons
```html
<button>This is a button</button> <!--Creates a button-->
```
### Properties
```html
<style>
	button {
		background-color: red; /*changes the background color*/
		color: blue; /*changes the color of the text*/
		border: 2px solid black; /*sets the border's style*/
		border-radius: 8px; /*for rounding corners*/
		padding: 10px; /*space between borders and text*/
		font-size: 10px;
		height: 50px;
		width: 50px;
		cursor: pointer; /*changes the pointer as it interacts with the button*/
		
	}
<\style>
```
## Paragraph
```html
<p>Paragraph of text<\p>
```
## Anchors
```html
<a>Text<\a>
```
### Attributes
#### `href`
```html
<a href = "external_link">Text<\a> <!--Creates a link to an external site-->
```
#### `target`
```html
<a target = "value">Text<\a> <!--Determines whether the link opens in the current space or in another tab>
```
### `class`
```html
<selector class = "name"><\selector> <!--Allows for naming of HTML objects-->
```
## CSS
```html
<style>
	selector {
		css_property = css_value;
		...
	}
	.element_name {
		...
		}
<\style>
```
### CSS Properties
```html
<style>
	selector {
		background-color = color_value; /*Colors the background*/
		color: color_value; /*Colors the object itself*/
		border: none; /*Gives the object a border (defaults to none)*/
		height: 1px; /*Determines the overall height of an object (in pixels)*/
		width: 1px; /*Determines the overall width of an object (in pixels)*/
		border-radius: 1px; /*Determines the width (radius) of its borders*/
		cursor: pointer;
	}
<\style>
```
### Color Values
```html
<style>
	selector {
		css_property = rgb(x, y, z);
		css_property = name_of_color; /*for example red, blue, green, etc. */
	}
</style>
```
where `x`, `y`, and `z` are the red, blue, and green values that make up a color respectively
##
# CSS