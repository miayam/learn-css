# Flexbox

![axis](./main-and-cross-axis.svg)

Flex container is an element with `display: flex`.
Flex items are direct children of flex container.

If you set `flex-direction` to `row`, flex items will sit next to each other like books in a bookshelf.

If you set `flex-direction` to `column`, flex items will stack on top of each other like floors in a building.

This imaginary line that `flex-direction` follows is called main axis.

Cross axis is the opposite of main axis.

Flex container can manipulate how its children behave with properties as follows:
* `justify-content`
* `align-items`
* `align-content`
* `flex-wrap`

Flex items can override styling imposed by flex container or adjust themselves inside the flex container as follows:
* `align-self`
* `order`
* `flex`
* `flex-shrink`
* `flex-grow`
* `flex-basis`
