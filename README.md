# Grid-and-Flexbox cheat sheet

# ▶️ Grid
🔸 The syntax for creating a grid:

```css
selection {
  display: grid; /* or inline-grid */
}
```

## Grid shorthand consists of the following properties with default values:

### <code>grid</code>

* A grid will allow you to organize the various elements on your page.

### <code>grid-template-rows</code>

* This property defines the size and number of rows in the grid.
```css
grid-template-rows: 100px 200px;
```
> [!NOTE]
> This creates two rows with heights of <sup>'100px'</sup> and <sup>'200px'</sup> respectively.

### <code>grid-template-columns</code>

* This property defines the size and number of columns in the grid.
```css
grid-template-columns: 1fr 2fr;
```
> [!NOTE]
> This creates two columns with width propertional to the available space, where the second column is twice as wide as the first.

### <code>grid-template-areas</code>

* This property allows you to define named grid areas asn specify how they are laid out in relation to each other.
```css
grid-template-areas:
  "header header"
  "sidebar main"
  "footer footer";
```
> [!NOTE]
> This creates a grid with three rows and two columns.
> The named areas <sup>"header"</sup>, <sup>"sidebar"</sup>, <sup>"main"</sup>, and <sup>"footer"</sup> define the layout of elements within the grid.

### <code>grid-auto-rows</code>

* This property sets the defayult size for rows that haven't been explicitly defined. 
```css
gird-auto-rows: minmax(100px, auto));
```
> [!NOTE]
> This sets the default height for unspecified rows to be a minimun of <sup>'100px'</sup> and expand to fit the content. 

### <code>grid-auto-columns</code>

* Similar to <sup>'grid-auto-rows'</sup>, this property sets the default width for columns that haven't been explicity defined. 
```css
grid-auto-columns: 100px;
```
> [!NOTE]
> This sets the default width for unspecified columns to <sup>'100px'</sup>.

### <code>grid-auto-flow</code>

* This property determines the default placement direction of grid items when they're not explicitly placed using grid-area or related properties.
```css
grid-auto-flow: row dense;
```
> [!NOTE]
> This sets the default location for grid items that are not explicitly allocated to follow the row leyout, and items are densely packed within the grid.

### <code>column-gap</code>

* This property sets the gap between columns.
```css
column-gap: 20px;
```
> [!NOTE]
> This sets a gap of <sup>'20px'</sup> between columns.

### <code>row-gap</code>

* This property set a gap between rows. 
```css
row-gap: 20px;
```
> [!NOTE]
> This sets a gap of <sup>'20px'</sup> between rows.

> [!TIP]
> An HTML and CSS example with each section seperated and labeled:
```html
<div class="grid-container">
    <div class="grid-item">1</div>
    <div class="grid-item">2</div>
    <div class="grid-item">3</div>
</div>
```
```css
/* Grid Container */
.grid-container {
    display: grid; /* Create a grid container */
    grid-template-rows: 100px 150px; /* Define two rows with heights of 100px and 150px */
    grid-template-columns: 1fr 2fr 1fr; /* Define three columns with flexible widths */
    grid-template-areas: 
        "header header header" /* Define grid areas for layout */
        "sidebar main main"; /* Define grid areas for layout */
    grid-auto-rows: auto; /* Default height for rows not explicitly sized */
    grid-auto-columns: auto; /* Default width for columns not explicitly sized */
    grid-auto-flow: row; /* Default flow for items placed on the grid */
    column-gap: 20px; /* Set gap between columns */
    row-gap: 10px; /* Set gap between rows */
}

/* Grid Items */
.grid-item {
    border: 1px solid black; /* Add border for visualization */
}
```

# ▶️ Grid properties for container

### <code>grid-template-columns</code>

* This property defines the size and number of columns in the grid.
* It accepts various units such as <sup>pixels ('px')</sup>, <sup>percentages ('%')</sup>, or the <sup>'repeat()'</sup> function for repetitive column sizes.
```css
grid-template-columns: 100px 1fr 2fr;
```
> [!NOTE]
> This creates three columns with sizes of <sup>'100px'</sup>, one fraction of the available space, and two fractions of the available space, respectively.

### <code>grid-template-rows:</code>

* This property defines the size and number of rows in the grid, similar to <sup>'grid-template-columns'</sup>.
```css
grid-template-rows: 100px 200px;
```
> [!NOTE]
> This creates two rows with heights of <sup>'100px'</sup> and <sup>'200px'</sup> respectively.

### <code>grid-auto-columns</code>

* This property sets the default size for columns that haven't been explicitly defined.
```css
grid-auto-columns: 50px;
```
> [!NOTE]
> This sets the default width for unspecified columns to <sup>'50px'</sup>.

### <code>grid-auto-rows</code>

* Similar to <sup>'grid-auto-columns'</sup>, this property sets the default height for rows that haven't been explicitly defined.
```css
grid-auto-rows: 1fr;
```
> [!NOTE]
> This sets the default height for unspecified rows to take up an equal share of the availabe space. 

### <code>grid-template</code>

* This shorthand property allows you to define the grid template in a single line, specifying both columns and rows along with their sizes.
```css
grid-template: "header header" auto
                "main right" 75vh
                "footer footer" 20rem;
```
> [!NOTE]
> This defines a grid with three rows and two columns, where the first row is auto sized, and second row takes up 75% of the viewport height, and the third row is <sup>'20rem'</sup> in height. The two columns are named <sup>"header"</sup> and <sup>"right"</sup>, respectively.

# ▶️ Gap

### <code>grid-gap</code>

* This is a shorthand property for setting the gap between rows and columns in a CSS Grid Layout.
```css
grid-gap: 10px 20px;
```
> [!NOTE]
> This sets a gap of <sup>'10px'</sup> between rows and <sup>'20px'</sup> between columns.

### <code>grid-column-gap</code>

* This property specifically determines the gap between columns.
```css
grid-column-gap: 15px;
```
> [!NOTE]
> This sets a gap of <sup>'15px'</sup> between columns.

### <code>grid-row-gap</code>

* This property specifically determines the gap between rows.
```css
grid-row-gap: 1em;
```
> [!NOTE]
> This sets a gap of '1em' between rows.

# ▶️ Alignment

### <code>justify-items</code>

* This property defines the default alignment of grid items along the inline (main) axis of the grid.
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
> [!NOTE]
> In this example, all grid items will be centered horizontally within their respective grid cells. 

### <code>align-items</code> 

* This property defines the default alignment of grid items along the block (cross) axis of the gird.
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
> [!NOTE]
> In this example, all grid items will be centered vertically within their respective grid cells. 

### <code>place-items</code>

* This shorthand property combines <sup>'justify-items'</sup> and <sup>'align-items'</sup> to  define the default alignment of grid items along both the inline and block axis of the grid. 
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
> [!NOTE]
> In this example, all grid items will be centered both horizontally and vetically within their respective grid cells.These alignment properties provide a convenient way to control the positioning of grid items within a CSS grid. Allowing for flexible and responsive layout. 








































