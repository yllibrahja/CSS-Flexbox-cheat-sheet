# ▶️ CSS Flexbox cheat sheet

### 1.1 [flex-direction property](#flex-direction-property)
### 1.2 [flex-wrap property](#flex-wrap-property)
### 1.3 [align-items property](#align-items-property)
### 1.4 [justify-content property](#justify-content-property)

### 2.1 [flex-grow property](#flex-grow-property)
### 2.2 [flex-shrink property](#flex-shrink-property)
### 2.3 [flex-basis property](#flex-basis-property)
### 2.4 [order property](#order-property)
### 2.5 [align-self property](#align-self-property)

## CSS Selectors

### Attribute Selectors
```css
[data-type="flex-container"] {
    display: flex; /* This makes the element a flex container */
}
```

### Class Selector
```css
.flex-container {
    display: flex; /* This makes the element a flex container */
}
```

### ID Selector
```css
#flex-container {
    display: flex; /* This makes the element a flex container */
}
```

### Type Selector
```css
div {
    display: flex; /* This makes all div elements flex containers */
}
```

### Universal Selector
```css
* {
    display: flex; /* This makes all elements flex containers */
}
```
```html
<!-- HTML Example -->
<div class="flex-container">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
</div>
```
### flex-direction property
```css
/* CSS for Flex Container */

/* flex-direction property */
.flex-container {
  display: flex;
  flex-direction: row; /* row | row-reverse | column | column-reverse */
}
```
> [!TIP]
> #### row:
> > Default value, Items are placed from left to right.
> #### row-reverse:
> > Items are placed from right to left.
> #### column:
> > Items are placed from top to bottom.
> #### column-revers:
> > Items are placed from bottom to top.

### flex-wrap property
```css
/* flex-wrap property */
.flex-container {
    display: flex;
    flex-wrap: wrap; /* wrap | nowrap */
}
```
>[!TIP]
> #### wrap:
>> Items wrap to the next line as needed
> #### nowrap:
>> Default value, Items are laid out in a single line. 

### align-items property
```css
/* align-items property */
.flex-container {
    display: flex;
    align-items: flex-start; /* flex-start | flex-end | center | stretch */
}
```
> [!TIP]
> #### flex-start:
> > Items are aligned to the start of the container *(top for row)*.
> #### flex-end:
> > Items are aligned to the end of the container *(bottom for row)*.
> #### center:
> > Items are centered in the container.
> #### stretch:
> > Items stretch to fill the container *(default)*.

### justify-content property
```css
/* justify-content property */
.flex-container {
    display: flex;
    justify-content: flex-start; /* flex-start | flex-end | center | space-between | space-evenly */
}
```
> [!TIP]
> #### flex-start:
> > Items are packed to the start *(left for row)*.
> #### flex-end:
> > Items are packed to the end *(right for row)*.
> #### center:
> > Items are centered.
> #### space-between:
> > Items are evenly distributed, first item at the start, last item at the end.
> #### space-evenly:
> > Items are evenly distributed with equal space around them.

## Flex Item Properties
```html
<!-- HTML Example -->
<div class="flex-container">
    <div class="flex-item">Item 1</div>
    <div class="flex-item">Item 2</div>
    <div class="flex-item">Item 3</div>
</div>
```
### flex-grow property
```css
/* CSS for Flex Items */

/* flex-grow property */
.flex-item {
    flex-grow: 1; /* factor of flex's main size */
}
```
> [!TIP]
> #### flex-grow:
> > Defines the ability for a flex item to grow if necessary.
> #### flex-grow: 1;
> > Means the item can grow to fill the available space proportionally. 
> #### flex-grow: 2;
> > Item will grow twice as much as items with flex-grow: 1.

### flex-shrink property
```css
/* flex-shrink property */
.flex-item {
    flex-shrink: 1; /* factor of flex's main size */
}
```
> [!TIP]
> #### flex-shrink:
> > Defines the ability for a flex item to shrink if necessary.
> #### flex-shrink: 1;
> > The item can shrink to fill the container.
> #### flex-shrink: 0;
> > Item will not shrink.

### flex-basis property
```css
/* flex-basis property */
.flex-item {
    flex-basis: auto; /* auto | specific size (e.g., 50px, 20%) */
}
```
> [!TIP]
> #### flex-basis:
> > Defines the initial main size of a flex item.
> #### flex-basis: auto;
> > Default, size based on content.
> #### flex-basis: 100px;
> > Item has a base size of 100px.

### order property
```css
/* order property */
.flex-item {
    order: 1; /* Set the order of the item */
}
```
> [!TIP]
> #### order:
> > Specifies the order of the flex items.
> #### order: 0;
> > Default, items appear in source order.
> #### order: 1;
> > Item apears after items with oder: 0.

### align-self property
```css
/* align-self property */
.flex-item {
    align-self: flex-start; /* auto | flex-start | flex-end | center | stretch */
```
> [!TIP]
> #### auto:
> > Default, Inherits align-items of the container.
> #### flex-start:
> > Aligns item to the start of the container.
> #### flex-end:
> > Aligns item to the end of the container.
> #### center:
> > Aligns item to the center of the container.
> #### stretch:
> > Stretches item to fill the container. 

> ## ▶️ Small project that demonstrates the use of all the Flexbox properties included in the cheat sheet. 

> * We'll create a simple HTML page with a flex container that includes multiple flex items, each demonstrating different properties.

## Project Structure
```
flexbox-demo/
├── index.html
└── styles.css
```
## HTML Structure
> [!NOTE]
> The HTML file includes a `div` with the class `flex-container` which contains five `div` elements, each with the class `flex-item` and unique class names for demonstration purposes. 
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flexbox Demo</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="flex-container">
        <div class="flex-item item1">Item 1</div>
        <div class="flex-item item2">Item 2</div>
        <div class="flex-item item3">Item 3</div>
        <div class="flex-item item4">Item 4</div>
        <div class="flex-item item5">Item 5</div>
    </div>
</body>
</html>
```
## CSS Styles
> [!NOTE]
> The base styles set up a simple centered layout with some basic styling.
>
> > The `.flex-container` class includes properties such as `flex-direction`, `flex-wrap`, `justify-content`, and `align-items` to demonstrate various Flexbox container properties.
>
> > The `.flex-item` class includes properties such as `flex-grow`, `flex-shrink`, and `flex-basis` to demonstrate Flexbox item properties.
>
> > Specific item classes (`.item1`, `.item2`, etc) demonstrate the `order` and `align-self` properties.
>
> > A hover effect is included to demonstrate dynamic changes in `flex-grow` and `flex-shrink`. 
```css
/* Base styles for the project */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f0f0f0;
}

/* Flex container styles */
.flex-container {
    display: flex;
    flex-direction: row; /* Change to row-reverse, column, column-reverse to see the effect */
    flex-wrap: wrap; /* Change to nowrap to see the effect */
    justify-content: space-between; /* Change to flex-start, flex-end, center, space-evenly to see the effect */
    align-items: center; /* Change to flex-start, flex-end, stretch to see the effect */
    width: 80%;
    height: 60%;
    border: 2px solid #ccc;
    background-color: #fff;
    padding: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

/* Flex item styles */
.flex-item {
    flex-grow: 1; /* Change to different values to see the effect */
    flex-shrink: 1; /* Change to different values to see the effect */
    flex-basis: 20%; /* Change to different values or units to see the effect */
    margin: 10px;
    padding: 20px;
    background-color: #007bff;
    color: #fff;
    text-align: center;
    border-radius: 5px;
    transition: all 0.3s ease;
}

/* Specific item styles */
.item1 {
    order: 2; /* Change to different values to see the effect */
    align-self: flex-start; /* Change to auto, flex-end, center, stretch to see the effect */
}

.item2 {
    order: 1;
    align-self: flex-end;
}

.item3 {
    order: 3;
    align-self: center;
}

.item4 {
    order: 4;
    align-self: stretch;
}

.item5 {
    order: 5;
    align-self: flex-start;
}

/* Hover effect to see flex-grow and flex-shrink in action */
.flex-item:hover {
    flex-grow: 2;
    flex-shrink: 0;
    background-color: #0056b3;
}
```
> [!IMPORTANT]
> ### This project provides a visual representation of the Flexbox properties and can be easily modified to experiment with different settings.









































