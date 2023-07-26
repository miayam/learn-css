# Logical Properties

Imagine you have a chessboard in front of you, with different squares and pieces on it. Each square has a specific position and rules associated with it. In this analogy, the chessboard represents the HTML structure of a webpage, and the squares and pieces represent different elements and their properties.

Now, when playing chess, you may encounter situations where the direction of the game changes. For example, you might start playing from one side of the board and then switch to playing from the opposite side. Similarly, in web development, you may need to handle different writing modes, such as left-to-right (LTR) or right-to-left (RTL) languages, which affect the layout and positioning of elements on a webpage.

Logical properties in CSS provide a way to describe the layout and positioning of elements based on the logical direction of the content, regardless of the physical direction. It refers to the edges of a box as they relate to the *flow of content*. It's like making moves on the chessboard based on the changing direction of the game. So, left, right, top, and bottom are relative to which side you are on.

## Block Flow
When the chessboard is flipped upside down, the top becomes the bottom, and vice versa. The logical properties for top and bottom will be block-start and block-end, respectively. For instance, `margin-top` will be `margin-block-start`, and `margin-bottom` will be `margin-block-end`.

## Inline Flow
When we invert the chessboard, the left side becomes the right, and vice versa. The logical properties for left and right will change to `inline-start` and `inline-end`.

## Flow Relative
![flow-relative](https://web-dev.imgix.net/image/VbAJIREinuYvovrBzzvEyZOpw5w1/GezxDZXkJgkMevkKg39M.png?auto=format&w=964)

## Sizing
The `block-size` CSS property defines the horizontal or vertical size of an element's block, depending on its writing mode. It's equivalent to `height` in normal flow.

The `inline-size` CSS property defines the horizontal or vertical size of an element's block, depending on its writing mode. It's equivalent to `width` in normal flow.

## Start and End

## Spacing and Positioning

## Borders

## Units

## Using Logical Properties Pragmatically
