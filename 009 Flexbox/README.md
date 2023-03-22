# Flexbox

Flex container is an element with `display: flex`.

Flex items are direct children of flex container.

If you set `flex-direction` to `row`, flex items will sit next to each other like books in a bookshelf.

If you set `flex-direction` to `column`, flex items will stack on top of each other like floors in a building.

This imaginary line that `flex-direction` follows is called main axis.

Cross axis is the opposite of main axis.

Main axis is connected to writing mode and script direction. For example in Arabic, inside a flex container with `flex-direction: row` applied, flex items will sit next to each other like books in a bookself from right to left. While in Japanese (kanji), flex items will stack on top of each other like floors in the building.

Flexbox is one-dimensional. You can control alignment and distribute space in one axis, a row or a column.

Along the main axis, you can distribute space with `justify-content` and `align-content` for a wrapped flex container. `place-content` is a shorthand for setting both properties.

Here's the explanation about `justify-content` from ChatGPT:

> Well, when we talk about "justify-content" in web design, we're talking about how to arrange things that are in a line, like those friends. The different values of justify-content tell the computer how to arrange those things.
>
> For example, if we use the "flex-start" value for justify-content, it's like asking the computer to line up the friends in a line and have them all stand against the left edge of the line. This is kind of like when the teacher lines up the class and tells everyone to stand in a straight line.
>
> If we use the "center" value for justify-content, it's like asking the computer to line up the friends in a line and have them all stand in the middle of the line. This is like when everyone tries to position themselves to be equidistant from both sides.
>
> And if we use the "flex-end" value for justify-content, it's like asking the computer to line up the friends in a line and have them all stand against the right edge of the line. This is like when everyone tries to position themselves at the end of the line closest to where they need to go next.
>
> There are a few other values for justify-content too, like "space-between" which puts equal space between each friend, and "space-around" which puts equal space between each friend and also puts some space on the left and right ends of the line.
>
> Finally, "space-evenly" would be like spreading out the toys so that there is the same amount of space between each one, creating an evenly spaced arrangement.

Here's the explanation about `align-content` from ChatGPT:

> In other words, if you have a container with multiple rows of flex items, "align-content" allows you to control the spacing between the rows along the vertical axis, such as how much space there is between each row of items.
>
> The available values for "align-content" include "flex-start", "flex-end", "center", "space-between", "space-around", "stretch", and "baseline". These values work in a similar way to "justify-content", but instead of aligning items horizontally, they align items vertically.

Along the cross axis, you can align flex items with `align-items` and `align-self`.

Here's the explanation about `align-items` and `align-self` from ChatGPT:

> "align-items" is a CSS property that controls how flex items are aligned along the cross-axis in the flex container. It is similar to "justify-content", but while "justify-content" controls horizontal alignment, "align-items" controls vertical alignment.
>
> For example, if you have a flex container with multiple rows of items, "align-items" will control how the items are vertically aligned within each row. The available values for "align-items" include "flex-start", "flex-end", "center", "baseline", and "stretch".
> 
> * "flex-start" aligns the items at the beginning of the container.
> * "flex-end" aligns the items at the end of the container.
> * "center" aligns the items at the center of the container.
> * "baseline" aligns the items such that their baselines align with each other.
> * "stretch" stretches the items to fill the container vertically.
>
> On the other hand, "align-self" is a CSS property that allows you to control the vertical alignment of a single flex item within the flex container. This property applies only to a single item, while "align-items" applies to all items in the container.
>
> The available values for "align-self" are the same as "align-items", but apply only to the item to which "align-self" is applied. For example, you might set "align-self: center" on a single item to center it vertically within its row, while leaving the other items aligned to the top or bottom of the row using "align-items".

Assume flex container has more space than is needed. How do flex items absorb the remaining space inside?

`flex-grow`, `flex-shrink`, and `flex-basis` are properties to control space inside flex items. `flex` is a shorthand for setting those properties.

`flex: initial` will make flex items do not grow, can shrink smaller than their `flex-basis` which is the size of their content.

`flex: auto` will make flex items space shared out after each item is laid out as max-content size. They will take up space but with different size.

`flex: 1` will make flex items space shared equally.