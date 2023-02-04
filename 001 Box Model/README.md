# Box Model

Everything you see on a web page is a box. All elements are boxes.

You can size the element as you like or let the browser discovers the right sizing for you.

Extrinsic sizing is when you size the element explicitly and set the fixed boundary to your
content. If the content is much bigger than the element, it will overflow.

What does overflow look like?

```

  * * * * * *
  *         *
  *   CSS is*the best
  *         *
  * * * * * *

```

Intinsic sizing is when you let the browser decide the right sizing for you based on your
content. The element will contract or expand as the content's size changed. It will not
overflow.

All boxes consist of content box, padding box, border box, and margin box. Those 4 types of boxes make up
an element on the page.

Content box is like an artwork.

Padding box is like a white space between the frame and the artwork.

Border box is like a frame that contains the artwork.

Margin box is the space between each frame.

## Control The Box Model

You can control how the box displayed by setting a value to `display` property in CSS.
* `inline` will take up space as much as its content needed.
* `block` will take up the whole space horizontally.
* `inline-block` will take up space as much as its content needed but behaves like a `block`.
* `grid`, `flex`, `inline-flex`, `inline-grid` require more than a paragraph to explain. More on that later.

You can also control the sizing of the box by setting a value to `box-sizing` property in CSS.
* `content-box` means padding's size and border's size will add up to make up an element's size. So 200px for the content + 40px of padding + 20px of border makes a total visible width of 260px.
* `border-box` means padding's size and border's size get pushed in and they will not add up to an element's size. So 200px for the content + 40px of padding + 20px of border makes a total visible width of 200px.