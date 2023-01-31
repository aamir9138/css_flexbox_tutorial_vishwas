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
