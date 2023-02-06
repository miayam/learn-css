# Layout

Back in early 90s, you can only use `<table>` to layout a web page.
Now, you've got modern CSS at your disposal.

First of all, we must understand what `display` property does
to an element.

The `display` property describes how an element flows on the page and how
its child elements behave. We've been introduced to `inline` and `block`
elements:

* `inline` will take up space as much as its content needed and sit next to each other.
* `block` will take up the whole space horizontally.

I think ChatGPT explains it better. Here's what it says:
> The `display` property in CSS determines how an HTML element should be displayed on the web page. It specifies the layout of the element and whether it should be a block-level or inline element.
> The `display` property can have several values, including:
>
> `block`: the element generates a block-level box, which means it takes up the full width of its parent container and creates a new line after the element. Block-level elements include div, h1, p, etc.
>
>`inline`: the element generates an inline-level box, which means it takes up only as much width as needed and does not create a new line after the element. Inline-level elements include span, a, strong, etc.
>
>`inline-block`: the element generates a box that is both inline-level and block-level, meaning it takes up only as much width as needed and creates a new line after the element.
>
>`none`: the element will not be displayed on the web page and will take up no space.
>
>`flex`: the element generates a flexible container for distributing space among its children.
>
>`grid`: the element generates a grid container for arranging its children into rows and columns.
>
>It's important to note that the display property can have a significant impact on the layout and appearance of a web page, so it's important to use it carefully and consistently throughout the stylesheet.

## Manipulate Child Elements With Flexbox And Grid
Flexbox and grid are `block` elements on steroid.

### Flexbox
```css
div {
  display: flex;
}
```
Think a box that contains items you can manipulate how they group inside.
You can make them either sit next to each other like books in a bookshelf
or stack on each other like floors in a building.

### Grid
```css
div {
  display: grid;
}
```
It's a `block` element with super powers. Its child elements can be thought of
as vehicles arranged in the parking lot. It suddenly has rows and columns.
You need bigger area for trucks, smaller one for motorbikes, etc, etc. Magic! 

## Manipulate How An Element Flow Inside A Container

### Inline Block
```css
span {
  display: inline-block;
}
```
It's an `inline` element on steroid. It respects styling that apply to `block`
element. Pretty neat!

### Floats
```css
img {
  float: left;
}
```
Have you seen a paragraph that wraps around the image like you might see in a newspaper? 
Yes, you can do that too on the web page.

### Multi Column List
```html
<ul>
  <li>Afghanistan</li>
  <li>Aland Islands</li>
  <li>Albania</li>
  <li>Algeria</li>
  <li>American Samoa</li>
  <li>Andorra</li>
  <li>Angola</li>
  <li>Anguilla</li>
  <li>Antarctica</li>
  <li>Antigua and Barbuda</li>
  <li>Argentina</li>
</ul>
```

```css
ul {
  column-count: 2;
  column-gap: 1em;
}
```
Normally, a list goes from top to bottom. One direction. With `column-count`, you can
make them splits into two. Imagine!

## Manipulate The Element's Position
We can get an element out of its flow. What does that mean?

Well, normally, an element stacks next to each other either
horizontally or vertically as it's written but somehow you want to make
it sticks on top as you scroll down. How? Worry not! We have
`position` property.

There are 5 possible values. These explanations are stolen from [w3schools.com](https://www.w3schools.com/css/css_positioning.asp):
* HTML elements are positioned `static` by default
* An element with `position: relative;` is positioned relative to its normal position
* An element with `position: absolute;` is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like `fixed`)
* An element with `position: fixed`; is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled
* An element with `position: sticky;` is positioned based on the user's scroll position. It becomes sticky when the scroll bar touches it
