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

### 🟧 1. grid-container
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
#### Explanation:
> [!NOTE]
> In this example, we have a container with the class <code>'grid-container'</code>, which is styled as a grid container using <code>'display: grid;'</code>.
> Inside the container, there are three grid items with the class <code>'grid-item'</code>.

### 🟧 2. grid-template-rows
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
#### Explanation:
> [!NOTE]
> Here, we have defined three rows with heights of <code>100px</code>, <code>150px</code>, and <code>200px</code> respectively using <code>grid-template-rows</code>.

### 🟧 3. grid-template-column
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
#### Explanation:
> [!NOTE]
> This example defines three columns with flexible widths using <code>'grid-template-columns'</code>. The first column takes up one fraction of the available space, the second takes up two fractions, and the third takes up one fraction.

### 🟧 4. grid-template-area
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
#### Explanation:
> [!NOTE]
> Here, we've defined named grid areas for a typical webpage layout, including <code>header</code>, <code>sidebar</code>, <code>main content</code>, and <code>footer</code>.

### 🟧 5. grid-auto-rows / grid-auto-columns
* We'll set default sizes for rows and columns using <code>'grid-auto-rows'</code> and <code>'grid-auto-columns'</code>.
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
#### Explanation:
> [!NOTE]
> This example sets default heights for rows and widths for columns that haven't been explicitly sized.

### 🟧 6. grid-auto-flow
* We'll specify the default placement direction for items using <code>'grid-auto-flow'</code>.
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
#### Explanation:
> [!NOTE]
> Here, we've specified the default placement direction for items on the grid as columns. Items will be added to the grid in a column-wise order.

### 🟧 7. column-gap / row-gap
* We'll set gaps between columns and rows using <code>'column-gap'</code> and <code>'row-gap'</code>.
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
#### Explanation:
> [!NOTE]
> This example sets a gap of 20px between columns and 10px between rows.

> [!TIP]
> These examples cover each section of the CSS Grid properties with simple explanations. You can combine these properties in various ways to create complex and responsive grid layout. 

# ▶️ Grid properties for container

### 🟦 1. grid-template-columns / grid-template-rows
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
#### Explanation:
> [!NOTE]
> <code>'grid-template-columns'</code> and <code>'grid-template-rows'</code> define the sizes of the columns and rows respectively within the grid.
> Can accept different measurement units such as pixels <code>('px')</code>, percentages <code>('%')</code>, or the auto <code>'auto'</code> keyword.
> In this example, the container has three columns with widths of <code>100px</code>, <code>200px</code>, and <b>automatically<b> adjusting to the content size respectively. It has two rows with heights of <code>50px</code> and <code>100px</code> respectively.

### 🟦 2. grid-auto-columns / grid-auto-rows
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
#### Explanation:
> [!NOTE]
> <code>'grid-auto-columns'</code> and <code>'grid-auto-rows'</code> determine the default size for columns and rows respectively that have not been explicitly defined.
> In this example, all columns will have a width of <code>150px</code> and all rows will have a height of <code>100px</code> by default.

### 🟦 3. grid-template
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
#### Explanation:
> [!NOTE]
> <code>'grid-template'</code> allows you to define the grid structure by specifying the names of grid areas and their sizes.
> In this example, the grid has three rows and two columns. The first row contains the header, the second row contains the main content and the right sidebar, and the third row contains the footer.
> The sizes of the rows are specified using different units <code>('vh')</code> and <code>('rem')</code>.

# ▶️ Gap

### 🟥 1. grid-gap
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
#### Explanation:
> [!NOTE]
> <code>'grid-gap'</code> determines the gap between rows and columns within the grid.
> It accepts different measurement units such as pixels <code>('px')</code>, percentages <code>('%')</code>, etc.
> In this example, there will be a <code>20px</code> gap between rows and columns.

### 🟥 2. grid-column-gap
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
#### Explanation:
> [!NOTE]
> <code>'grid-column-gap'</code> determines the gap between columns within the grid.
> It accepts different measurement units such as pixels <code>('px')</code>, percentages <code>('%')</code>, etc.
> In this example, there will be a <code>30px</code> gap between columns.

### 🟥 3. grid-row-gap
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
#### Explanation:
> [!NOTE]
> <code>'grid-row-gap'</code> determines the gap between rows within the grid.
> It accepts multiple values, each representing the gap between adjacent rows.
> In this example, there will be a gap of <code>10px</code> between the first and second rows, and a gap of <code>20px</code> between the second and third rows. 

# ▶️ Alignment

### 🟩 1. justify-items
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
#### Explanation:
> [!NOTE]
> <code>'justify-items'</code> defines the default space that is allotted to each item on the grid along the inline axis (horizontally).
> Values can be <code>'start'</code>, <code>'center'</code>, <code>'end'</code>, or <code>'stretch'</code>.
> In this example, items will be aligned to the start of the grid along the inline axis.

### 🟩 2. align-items
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
#### Explanation:
> [!NOTE]
> <code>'align-items'</code> defines the default space related to an item along the grid's block axis (vertically).
> Values can be <code>'start'</code>, <code>'center'</code>, <code>'end'</code>, or <code>'stretch'</code>.
> In this example, items will be aligned to the start of the grid along the block axis.


### 🟩 3. place-items
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
#### Explanation:
> [!NOTE]
> <code>'place-items'</code> is a shorthand property for <code>'justify-items'</code> and <code>'align-items'</code>.
> It allows to align items with the block and inline directions simultaneously.
> In this example, items wil be aligned to the start along the inline axis and streched along the block 








































