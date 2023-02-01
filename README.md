## lecture 1 Introduction

### What is Flexbox?

CSS Flexible Box Module is a one dimensional layout model which makes it easy to build

- flexible and efficient layouts
- distribute space among items
- control their alignment

### Layout modes

Before flexbox there were 4 layout modes

1. `Block`, for sections in a webpage.
2. `inline`, for text
3. `Table`, for two dimensional table data
4. `Positioned`, for explicit position of an element

but these layout didnot provide enough flexibility

### Why Flexbox?

1. a lot of flexibility
2. arrange items
3. spacing
4. alignment
5. order of items
6. bootstrap 4 is built on top of the flex layout

## lecture 2 Terminology

### Two entities

When we talk about flexbox we mainly have 2 entities.

1. A parent container which we term as `Flex Container`
2. And the immediate children elements which we term as `Flex Items`

![flex container and flex items](./pictures/flexContainer_flexItems.PNG)

here the div with class container is `flex container` and the div with items are `flex items`

### Two axis

we have 2 axis in flexbox

1. `Main Axis` (by default runs horizantal from left to right)
2. `Cross Axis` (by default runs perpendicular from top to bottom)

- The starting point of the main axis is termed as `main start` and end point is `main end`.
- The length from `main start` and `main end` is `main size`.

So we can say that the flex items flow from `main start` till `main end` and take up the main size as the length.
Similar for the Cross axis `cross start` is at the top and `cross end` is at the bottom.

![flexbox axis](./pictures/flexbox_axis.PNG)

We can change the direction but we will talk about this later.

## lecture 3 Flex Container Properties

in this we will see all the properties related to `flex container`

1. `display` : This is what define a flex container and is `mandatory` to work with flex container
2. `flex-direction`: define the direction of flex items placed in a `flex container`.
3. `flex-wrap` : which is used to control the wrapping of items within a `flex container`.
4. `flex-flow`: a shorthand for the `flex-direction` and `flex-wrap`.
5. `justify-content`: it define the alignment of the items along the `main axis`
6. `align-items`: it defines how the `flex items` are laid along the `cross axis`
7. `align-content`: this is similar to `justify-content` the only difference is that it will do it along the `cross axis` instead of `main axis`. also `align-content` works only if we have multiple rows

## lecture 4 Flex display

1. create an html file `index.html`

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="container">
    <div class="flex-item item-1">Item 1</div>
    <div class="flex-item item-2">Item 2</div>
    <div class="flex-item item-3">Item 3</div>
    <div class="flex-item item-4">Item 4</div>
    <div class="flex-item item-5">Item 5</div>
    <div class="flex-item item-6">Item 6</div>
    <div class="flex-item item-7">Item 7</div>
    <div class="flex-item item-8">Item 8</div>
    <div class="flex-item item-9">Item 9</div>
  </div>
</body>
</html>
```

2. create a `styles.css` file

```
body{
  margin: 0;
}
.container{
  border: 6px solid black
}
.flex-item{
  color: white;
  font-size: 1.5rem;
  padding: 1rem;
  text-align: center;

}
.item-1 {
  background-color: #B4BF35;
}
.item-2 {
  background-color: #B95F21;
}
.item-3 {
  background-color: #1C4C56;
}
.item-4 {
  background-color: #CfB276;
}
.item-5 {
  background-color: #6B0803;
}
.item-6 {
  background-color: #1C4C56;
}
.item-7 {
  background-color: #B95F21;
}
.item-8 {
  background-color: #01243A;
}
.item-9 {
  background-color: #AAD041;
}
```

The result will be like as under

![initial setup](./pictures/html_and_css_initial.PNG)

now when we apply the `display: flex` property on the `flex container`

```
.container{
  border: 6px solid black;
  display: flex;
}
```

The result is like so
![display flex](./pictures/display_flex.PNG)

so if we see the `flex container` is taking the full block width and all the child items will take some space.

if we want the `flex container` not to take the block space only the `inline` space than we have to to specify as `display: flex-inline` and the result is as under.

![inline flex](./pictures/inline_flex.PNG)

so to sum up `display` either creates either a block level or inline level flex container.

1. `display: flex`
2. `display: inline-flex`

## lecture 5 flex direction

It sets the direction of the `main axis`. we have 4 major types for it.

1. `flex-direction: row` the default
2. `flex-direction: row-reverse` main axis change from `left to right` to `right to left`
3. `flex-direction: column` main axis change to `top to bottom`
4. `flex-direction: column-reverse` main axis change to `bottom to top`
