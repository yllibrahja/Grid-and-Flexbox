# CSS Grid cheat sheet

## ▶️ Grid
### 1.1 [grid-container](#grid-container)
### 1.2 [grid-template-rows](#grid-template-rows)
### 1.3 [grid-template-column](#grid-template-column)
### 1.4 [grid-template-area](#grid-template-area)
### 1.5 [grid-auto-rows / grid-auto-columns](#grid-auto-rows--grid-auto-columns)
### 1.6 [grid-auto-flow](#grid-auto-flow)
### 1.7 [column-gap / row-gap](#column-gap--row-gap)

## ▶️ Grid properties for container
### 2.1 [grid-template-columns / grid-template-rows](#grid-template-columns--grid-template-rows)
### 2.2 [grid-auto-columns / grid-auto-rows](#grid-auto-columns--grid-auto-rows)
### 2.3 [grid-template](#grid-template)

## ▶️ Gap
### 3.1 [grid-gap](#grid-gap)
### 3.2 [grid-column-gap](#grid-column-gap)
### 3.3 [grid-row-gap](#grid-row-gap)

## ▶️ Alignment
### 4.1 [justify-items](#justify-items)
### 4.2 [align-items](#align-items)
### 4.3 [place-items](#place-items)

## ▶️ Justification
### 5.1 [justify-content](#justify-content)
### 5.2 [align-content](#align-content)
### 5.3 [place-content](#place-content)

## ▶️ Positioning
### 6.1 [grid-auto-flow](#grid-auto-flow)
### 6.2 [grid-auto-columns](#grid-auto-columns)
### 6.3 [grid-auto-rows](#grid-auto-rows)

## ▶️ Grid properties for items (child)
### 7.1 [grid-column](#grid-column)
### 7.2 [grid-column-start / grid-column-end](#grid-column-start--grid-column-end)
### 7.3 [grid-row](#grid-row)
### 7.4 [grid-row-start / grid-row-end](#grid-row-start--grid-row-end)

## ▶️ Justification and Alignment
### 8.1 [justify-self](#justify-self)
### 8.2 [align-self](#align-self)
### 8.3 [place-self](#place-self)

### grid-container
```html
<div class="grid-container">
    <div class="grid-item">1</div>
    <div class="grid-item">2</div>
    <div class="grid-item">3</div>
</div>
```
```css
.grid-container {
    display: grid; /* Create a grid container */
    /* Other grid properties can be added here */
}
.grid-item {
    /* Styles for grid items */
}
```
> [!NOTE]
> In this example, we have a container with the class `'grid-container'`, which is styled as a grid container using `'display: grid;'`.
> > Inside the container, there are three grid items with the class `'grid-item'`.

### grid-template-rows
* This property defines the size and number of rows in the grid.
```html
<div class="grid-container">
    <div class="grid-item">1</div>
    <div class="grid-item">2</div>
    <div class="grid-item">3</div>
</div>
```
```css
.grid-container {
    display: grid;
    grid-template-rows: 100px 150px 200px; /* Define three rows with specific heights */
}
```
> [!NOTE]
> Here, we have defined three rows with heights of `100px`, `150px`, and `200px` respectively using `grid-template-rows`.

### grid-template-column
* This property defines the size and number of columns in the grid. 
```html
<div class="grid-container">
    <div class="grid-item">1</div>
    <div class="grid-item">2</div>
    <div class="grid-item">3</div>
</div>
```
```css
.grid-container {
    display: grid;
    grid-template-columns: 1fr 2fr 1fr; /* Define three columns with flexible widths */
}
```
> [!NOTE]
> This example defines three columns with flexible widths using `'grid-template-columns'`.
> > The first column takes up one fraction of the available space, the second takes up two fractions, and the third takes up one fraction.

### grid-template-area
* This property allows you to define named grid areas and specify how they are laid out in relation to each other. 
```html
<div class="grid-container">
    <div class="grid-item">1</div>
    <div class="grid-item">2</div>
    <div class="grid-item">3</div>
</div>
```
```css
.grid-container {
    display: grid;
    grid-template-areas:
        "header header header"
        "sidebar main main"
        "footer footer footer"; /* Define grid areas for layout */
}
```
> [!NOTE]
> Here, we've defined named grid areas for a typical webpage layout
> > including `header`, `sidebar`, `main content`, and `footer`.

### grid-auto-rows / grid-auto-columns
* We'll set default sizes for rows and columns using `'grid-auto-rows'` and `'grid-auto-columns'`.
```html
<div class="grid-container">
    <div class="grid-item">1</div>
    <div class="grid-item">2</div>
    <div class="grid-item">3</div>
</div>
```
```css
.grid-container {
    display: grid;
    grid-auto-rows: 100px; /* Default height for rows not explicitly sized */
    grid-auto-columns: 50px; /* Default width for columns not explicitly sized */
}
```
> [!NOTE]
> This example sets default heights for rows and widths for columns that haven't been explicitly sized.

### grid-auto-flow
* We'll specify the default placement direction for items using `'grid-auto-flow'`.
```html
<div class="grid-container">
    <div class="grid-item">1</div>
    <div class="grid-item">2</div>
    <div class="grid-item">3</div>
</div>
```
```css
.grid-container {
    display: grid;
    grid-auto-flow: column; /* Default location for items placed on the grid */
}
```
> [!NOTE]
> Here, we've specified the default placement direction for items on the grid as columns.
> > Items will be added to the grid in a column-wise order.

### column-gap / row-gap
* We'll set gaps between columns and rows using `'column-gap'` and `'row-gap'`.
```html
<div class="grid-container">
    <div class="grid-item">1</div>
    <div class="grid-item">2</div>
    <div class="grid-item">3</div>
</div>
```
```css
.grid-container {
    display: grid;
    column-gap: 20px; /* Set gap between columns */
    row-gap: 10px; /* Set gap between rows */
}
```
> [!NOTE]
> This example sets a gap of 20px between columns and 10px between rows.

> [!TIP]
> These examples cover each section of the CSS Grid properties with simple explanations.
> > You can combine these properties in various ways to create complex and responsive grid layout. 

# ▶️ Grid properties for container

### grid-template-columns / grid-template-rows
```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
  <div class="item">Item 3</div>
</div>
```
```css
.container {
  display: grid;
  /* Define the sizes of columns */
  grid-template-columns: 100px 200px auto; /* measurement units */
  /* Define the sizes of rows */
  grid-template-rows: 50px 100px; /* measurement units */
}

.item {
  border: 1px solid black;
}
```
> [!NOTE]
> `'grid-template-columns'` and `'grid-template-rows'` define the sizes of the columns and rows respectively within the grid.
>> Can accept different measurement units such as pixels (`'px'`), percentages (`'%'`), or the auto `'auto'` keyword.
> In this example, the container has three columns with widths of `100px`, `200px`, and automatically adjusting to the content size respectively.
>> It has two rows with heights of `50px`and `100px` respectively.

### grid-auto-columns / grid-auto-rows
```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
</div>
```
```css
.container {
  display: grid;
  /* Set default width for columns */
  grid-auto-columns: 150px; /* measurement unit (fixed value for all columns) */
  /* Set default height for rows */
  grid-auto-rows: 100px; /* measurement unit (fixed value for all rows) */
}

.item {
  border: 1px solid black;
}
```
> [!NOTE]
> `'grid-auto-columns'` and `'grid-auto-rows'` determine the default size for columns and rows respectively that have not been explicitly defined.
> > In this example, all columns will have a width of `150px` and all rows will have a height of `100px` by default.

### grid-template
```html
<div class="container">
  <div class="header">Header</div>
  <div class="main">Main Content</div>
  <div class="right">Right Sidebar</div>
  <div class="footer">Footer</div>
</div>
```
```css
.container {
  display: grid;
  /* Define the grid layout */
  grid-template: 
    "header header" auto
    "main right" 75vh
    "footer footer" 20rem;
}

.header, .main, .right, .footer {
  border: 1px solid black;
}
```
> [!NOTE]
> `'grid-template'` allows you to define the grid structure by specifying the names of grid areas and their sizes.<br>
> > In this example, the grid has three rows and two columns.
> > The first row contains the *header*, the second row contains the *main content* and the *right sidebar*, and the third row contains the *footer*.
> > > The sizes of the rows are specified using different units (`'vh'`) and (`'rem'`).

# ▶️ Gap

### grid-gap
```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
</div>
```
```css
.container {
  display: grid;
  /* Determine the gap between rows and columns */
  grid-gap: 20px; /* measurement units */
}

.item {
  border: 1px solid black;
}
```
> [!NOTE]
> `'grid-gap'` determines the gap between rows and columns within the grid. It accepts different measurement units such as pixels (`'px'`), percentages (`'%'`), etc.
> > In this example, there will be a `20px` gap between rows and columns.

### grid-column-gap
```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
</div>
```
```css
.container {
  display: grid;
  /* Determine the gap between columns */
  grid-column-gap: 30px; /* measurement units */
}

.item {
  border: 1px solid black;
}
```
> [!NOTE]
> `'grid-column-gap'`determines the gap between columns within the grid. It accepts different measurement units such as pixels (`'px'`), percentages (`'%'`), etc.
> > In this example, there will be a `30px` gap between columns.

### grid-row-gap
```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
</div>
```
```css
.container {
  display: grid;
  /* Determine the gap between rows */
  grid-row-gap: 10px 20px; /* m-unit-1 m-unit-2 */
}

.item {
  border: 1px solid black;
}
```
> [!NOTE]
> `'grid-row-gap'` determines the gap between rows within the grid. It accepts multiple values, each representing the gap between adjacent rows.
> > In this example, there will be a gap of `10px` between the first and second rows, and a gap of `20px` between the second and third rows. 

# ▶️ Alignment

### justify-items
```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
</div>
```
```css
.container {
  display: grid;
  justify-items: start; /* Defines the default space allotted to each item on the grid */
}

.item {
  border: 1px solid black;
}
```
> [!NOTE]
> `'justify-items'` defines the default space that is allotted to each item on the grid along the inline axis (horizontally).
> > Values can be `'start'`, `'center'`, `'end'`, or `'stretch'`.
> > > In this example, items will be aligned to the start of the grid along the inline axis.

### align-items
```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
</div>
```
```css
.container {
  display: grid;
  align-items: start; /* Defines the default space related to an item along the grid’s block axis */
}

.item {
  border: 1px solid black;
}
```
> [!NOTE]
> `'align-items'` defines the default space related to an item along the grid's block axis (vertically).
> > Values can be `'start'`, `'center'`>, `'end'`, or `'stretch'`.
> > > In this example, items will be aligned to the start of the grid along the block axis.


### place-items
```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
</div>
```
```css
.container {
  display: grid;
  /* Shorthand for justify-items and align-items */
  place-items: start stretch; 
}

.item {
  border: 1px solid black;
}
```
> [!NOTE]
> `'place-items'` is a shorthand property for `'justify-items'` and `'align-items'`.
> > It allows to align items with the block and inline directions simultaneously.
> > > In this example, items wil be aligned to the start along the inline axis and streched along the block 

# ▶️ Justification

### justify-content
```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
</div>
```
```css
.container {
  display: grid;
  justify-content: space-between; /* Defines browser allocation of space to content items in relation to the main-axis */
}

.item {
  border: 1px solid black;
}
```
> [!NOTE]
> `'justify-content'` defines how the browser allocates space to content items along the main axis of the grid container.<br>
> Values can be `'start'`, `'center'`, `'end'`, `'stretch'`, `'space-between'`, `'space-evenly'`, or `'space-around'`.
> > In this example, items will be evely distributed along the main axis with equal space between.

### align-content
```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
</div>
```
```css
.container {
  display: grid;
  align-content: center; /* Defines browser allocation of space to content items in relation to the cross axis and block axis */
}

.item {
  border: 1px solid black;
}
```
> [!NOTE]
> `'align-content'` defines how the browser allocates space to content items in relation to the cross axis and block asix of the grid container.<br>
> Values can be `'start'`, `'center'`, `'end'`, `'stretch'`, `'space-between'`, `'space-evenly'`, or `'space-around'`.
> > In this example, items will be centered along the corss axis and block axis.

### place-content
```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
</div>
```
```css
.container {
  display: grid;
  /* Shorthand for align-content and justify-content */
  place-content: center start; 
}

.item {
  border: 1px solid black;
}
```
> [!NOTE]
> `'place-content'` is a shorthand property for `'align-content'` and `'justify-content'`.<br>
> It allows you to align content items with the block and inline directions simultaneously.
> > In this example, items will be centered along the inline asix and aligned to the start along the block axis. 

# ▶️ Positioning

### grid-auto-flow
```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
  <div class="item">Item 3</div>
</div>
```
```css
.container {
  display: grid;
  grid-auto-flow: row; /* This relates to how the items are placed automatically within the grid */
}

.item {
  border: 1px solid black;
}
```
> [!NOTE]
> `'grid-auto-flow'` determines how items are placed automatically within the grid when there is no explicit positioning.<br>
> Values can be `'row'`, `'column'`, or `'dense'`.
> > In this example, items will be placed row by row within the grid.

### grid-auto-columns
```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
</div>
```
```css
.container {
  display: grid;
  grid-auto-columns: 100px; /* This relates to the size for columns created without specific size specifications */
}

.item {
  border: 1px solid black;
}
```
> [!NOTE]
> `'grid-auto-columns'` determines the default size for columns created without specific size specifications.<br>
> It accept different measurement units such as pixels (`'px'`), percentages (`'%'`), etc.
> > In this example, columns without specified size will have a width of <code>100px</code>.

### grid-auto-rows
```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
</div>
```
```css
.container {
  display: grid;
  grid-auto-rows: 50px; /* This relates to the size for rows created without specific size specifications */
}

.item {
  border: 1px solid black;
}
```
> [!NOTE]
> `'grid-auto-rows'` determines the default size for rows created without specific size specifications.<br>
> It accept different measurement units such as pixels (`'px'`), percentages (`'%'`), etc.
> > In this example, rows without specified size will have a width or `50px`.

# ▶️ Grid properties for items (child)

### grid-column
```html
<div class="container">
  <div class="item">Item</div>
</div>
```
```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr; /* Define grid columns */
}

.item {
  grid-column: 1 / 2; /* Specify where on the grid the column is to start */
  border: 1px solid black;
}
```
> [!NOTE]
> `'grid-column'` allows you to specify where on the grid the column of the item starts and ends.<br>
> the syntax is `'start / end'`, where start and end are column positions.
> > In this example, the item starts at the first column and ends at the second column. 

### grid-column-start / grid-column-end
```html
<div class="container">
  <div class="item">Item</div>
</div>
```
```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr; /* Define grid columns */
}

.item {
  grid-column-start: 1; /* Determine the starting column position */
  grid-column-end: 2; /* Determine the end column position */
  border: 1px solid black;
}
```
> [!NOTE]
> `'grid-column-start'` determines the starting column position of the item on the grid.<br>
> `'grid-column-end'` determines the ending column position of the item on the grid.
> > In this example, the item starts at the first column and ends at the second column.

### grid-row
```html
<div class="container">
  <div class="item">Item</div>
</div>
```
```css
.container {
  display: grid;
  grid-template-rows: 1fr 1fr; /* Define grid rows */
}

.item {
  grid-row: 1 / 2; /* Specify where on the grid the row is to start */
  border: 1px solid black;
}
```
> [!NOTE]
> `'grid-row'`allows you to specify where on the grid the row of the item starts and ends.<br>
> The syntax is `'start / end'`, where start and end are row positions.
> > In this example, the item starts at the first row and ends a the second row.

### grid-row-start / grid-row-end
```html
<div class="container">
  <div class="item">Item</div>
</div>
```
```css
.container {
  display: grid;
  grid-template-rows: 1fr 1fr; /* Define grid rows */
}

.item {
  grid-row-start: 1; /* Determine the starting row position */
  grid-row-end: 2; /* Determine the end row position */
  border: 1px solid black;
}
```
> [!NOTE]
> `'grid-row-start'` determines the starting row position of the item on the grid.<br>
> `'grid-row-end'` determines the ending row position of the item on the grid.
> > In this example, the item starts at the first row and ends at the second row.

# ▶️ Justification and Alignment

### justify-self
```html
<div class="container">
  <div class="item">Item</div>
</div>
```
```css
.container {
  display: grid;
}

.item {
  justify-self: start; /* Determines how an item is positioned inside its aligned container in relation to the appropriate axis */
  border: 1px solid black;
}
```
> [!NOTE]
> `'justify-self'` determines how an item is positioned inside its aligned container along the inline axis (horizontal for `'row'`, vertical for `'column'`).<br>
> Values can be `'start'`, `'center'`, `'end'`, or `'stretch'`.
> > In this example, the item will be aligned to the start of its grid cell along the inline axis.

### align-self
```html
<div class="container">
  <div class="item">Item</div>
</div>
```
```css
.container {
  display: grid;
}

.item {
  align-self: start; /* Aligns an item within a grid area */
  border: 1px solid black;
}
```
> [!NOTE]
> `'align-self'` aligns an item within its grid cell along the block axis (vertical for `'row'`, horizontal for `'column'`).<br>
> Values can be `'start'`, `'center'`, `'end'`, or `'stretch'`.
> > In this example, the item will be aligned to the start of its grid cell along the block axis

### place-self
```html
<div class="container">
  <div class="item">Item</div>
</div>
```
```css
.container {
  display: grid;
}

.item {
  place-self: start stretch; /* Shorthand for justify-self and align-self */
  border: 1px solid black;
}
```
> [!NOTE]
> `'place-self'` is a shorthand property for `'justify-self'` and `'align-self'`.<br>
> It allows to position and align an item within its grid cell along both the inline and block axes simultaneously.
> > In this example, the item will be aligned to the start along the inline axis and streched along the block axis. 




























