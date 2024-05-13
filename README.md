<h1>Grid-and-Flexbox cheat sheet</h1>

<h2> ➡️ Grid</h2>
<h3> 🔸 The syntax for creating a grid:</h3>

```css
selection {
  display: grid; /* or inline-grid */
}
```
<hr>
<h3> 🟠 Grid shorthand consists of the following properties with default values: 🟠 </h3>
<hr>

<code>grid</code>

&emsp; - A grid will allow you to organize the various elements on your page.

<code>grid-template-rows</code>

&emsp; ◽ This property defines the size and number of rows in the grid.
```css
grid-template-rows: 100px 200px;
```
&emsp; ▫️ This creates two rows with heights of '100px' and '200px' respectively.

<code>grid-template-columns</code>

&emsp; ◽ This property defines the size and number of columns in the grid.
```css
grid-template-columns: 1fr 2fr;
```
&emsp; ▫️ This creates two columns with width propertional to the available space, where the second column is twice as wide as the first.

<code>grid-template-areas</code>

&emsp; ◽ This property allows you to define named grid areas asn specify how they are laid out in relation to each other.
```css
grid-template-areas:
  "header header"
  "sidebar main"
  "footer footer";
```
&emsp; ▫️ This creates a grid with three rows and two columns. <br>
&emsp; ▫️ The named areas "header", "sidebar", "main", and "footer" define the layout of elements within the grid.

<code>grid-auto-rows</code>

&emsp; ◽ This property sets the defayult size for rows that haven't been explicitly defined. 
```css
gird-auto-rows: minmax(100px, auto));
```
&emsp; ▫️ This sets the default height for unspecified rows to be a minimun of '100px' and expand to fit the content. 

<code>grid-auto-columns</code>

&emsp; ◽ Similar to 'grid-auto-rows', this property sets the default width for columns that haven't been explicity defined. 
```css
grid-auto-columns: 100px;
```
&emsp; ▫️ This sets the default width for unspecified columns to '100px'.

<code>grid-auto-flow</code>

&emsp; ◽ This property determines the default placement direction of grid items when they're not explicitly placed using grid-area or related properties.
```css
grid-auto-flow: row dense;
```
&emsp; ▫️ This sets the default location for grid items that are not explicitly allocated to follow the row leyout, and items are densely packed within the grid.

<code>column-gap</code>

&emsp; ◽ This property sets the gap between columns.
```css
column-gap: 20px;
```
&emsp; ▫️ This sets a gap of '20px' between columns.

<code>row-gap</code>

&emsp; ◽ This property set a gap between rows. 
```css
row-gap: 20px;
```
&emsp; ▫️ This sets a gap of '20px' between rows.

<hr>
<h3> 🟠 Grid properties for container 🟠 </h3>
<hr>

<code>grid-template-columns</code>

&emsp; ◽ This property defines the size and number of columns in the grid.<br>
&emsp; ◽ It accepts various units such as pixels ('px'), percentages ('%'), or the 'repeat()' function for repetitive column sizes.
```css
grid-template-columns: 100px 1fr 2fr;
```
&emsp; ▫️ This creates three columns with sizes of '100px', one fraction of the available space, and two fractions of the available space, respectively.

<code>grid-template-rows:</code>

&emsp; ◽ This property defines the size and number of rows in the grid, similar to 'grid-template-columns'.
```css
grid-template-rows: 100px 200px;
```
&emsp; ▫️ This creates two rows with heights of '100px' and '200px' respectively.

<code>grid-auto-columns</code>

&emsp; ◽ This property sets the default size for columns that haven't been explicitly defined.
```css
grid-auto-columns: 50px;
```
&emsp; ▫️ This sets the default width for unspecified columns to '50px'.

<code>grid-auto-rows</code>

&emsp; ◽ Similar to 'grid-auto-columns', this property sets the default height for rows that haven't been explicitly defined.
```css
grid-auto-rows: 1fr;
```
&emsp; ▫️ This sets the default height for unspecified rows to take up an equal share of the availabe space. 

<code>grid-template</code>

&emsp; ◽ This shorthand property allows you to define the grid template in a single line, specifying both columns and rows along with their sizes.
```css
grid-template: "header header" auto
                "main right" 75vh
                "footer footer" 20rem;
```
&emsp; ▫️ This defines a grid with three rows and two columns, where the first row is auto sized,<br>
&emsp; ▫️ and second row takes up 75% of the viewport height, and the third row is '20rem' in height.<br>
&emsp; ▫️ The two columns are named "header" and "right", respectively.

<hr>
<h3> 🟠 Gap 🟠 </h3>
<hr>

<code>grid-gap</code>

&emsp; ◽ This is a shorthand property for setting the gap between rows and columns in a CSS Grid Layout.
```css
grid-gap: 10px 20px;
```
&emsp; ▫️ This sets a gap of '10px' between rows and '20px' between columns.

<code>grid-column-gap</code>

&emsp; ◽ This property specifically determines the gap between columns.
```css
grid-column-gap: 15px;
```
&emsp; ▫️ This sets a gap of '15px' between columns.

<code>grid-row-gap</code>

&emsp; ◽ This property specifically determines the gap between rows.
```css
grid-row-gap: 1em;
```
&emsp; ▫️ This sets a gap of '1em' between rows.

<hr>
<h3> 🟠 Alignment 🟠 </h3>
<hr>

<code>justify-items</code>

&emsp; ◽ This property defines the default alignment of grid items along the inline (main) axis of the grid.
```html
<div class="grid-container">
    <div class="grid-item">Item 1</div>
    <div class="grid-item">Item 2</div>
    <div class="grid-item">Item 3</div>
</div>
```
```css
.grid-container {
    display: grid;
    justify-items: center; /* Align items along the inline axis to the center */
}

.grid-item {
    /* Additional styling for grid items */
}
```
&emsp; ▫️ In this example, all grid items will be centered horizontally within their respective grid cells. 

<code>align-items</code> 

&emsp; ◽ This property defines the default alignment of grid items along the block (cross) axis of the gird.
```html
<div class="grid-container">
    <div class="grid-item">Item 1</div>
    <div class="grid-item">Item 2</div>
    <div class="grid-item">Item 3</div>
</div>
```
```css
.grid-container {
    display: grid;
    align-items: center; /* Align items along the block axis to the center */
}

.grid-item {
    /* Additional styling for grid items */
}
```
&emsp; ▫️ In this example, all grid items will be centered vertically within their respective grid cells. 

<code>place-items</code>

&emsp; ◽ This shorthand property combines 'justify-items' and 'align-items' to  define the default alignment of grid items along both the inline and block axis of the grid. 
```html
<div class="grid-container">
    <div class="grid-item">Item 1</div>
    <div class="grid-item">Item 2</div>
    <div class="grid-item">Item 3</div>
</div>
```
```css
.grid-container {
    display: grid;
    place-items: center; /* Align items along both axes to the center */
}

.grid-item {
    /* Additional styling for grid items */
}
```
&emsp; ▫️ In this example, all grid items will be centered both horizontally and vetically within their respective grid cells. <br>
&emsp; ▫️ These alignment properties provide a convenient way to control the positioning of grid items within a CSS grid. <br>
&emsp; ▫️ Allowing for flexible and responsive layout. 








































