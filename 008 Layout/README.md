# Layout

Back in early 90s, you can only use `<table>` to layout a web page.
Now, you've got modern CSS at your disposal.

First of all, we must understand what `display` property does
to an element.

The `display` property describes how an element flows on the page and how
its child elements behave. We've been introduce to `inline` and `block`
elements:

* `inline` will take up space as much as its content needed.
* `block` will take up the whole space horizontally.

## Manipulate How Child Elements Behave With Flexbox And Grid
Flexbox and grid are like a `block` element but each of which
has special abilities.

### Flexbox
```css
div {
  display: flex;
}
```
It requires more than a paragraph to explain. Think a box that
contains items and you can manipulate how they stack inside.
You can make them either stack horizontally or vertically.
It's flexible. It's a `block` element on steroid.

### Grid
```css
div {
  display: grid;
}
```
It's a `block` element with super powers. Its child elements can be manipulated
as if they are in x-y axis graph. It suddenly has rows and columns. Magic! 

## Manipulate How An Element Flow Inside A Parent Element

### Inline Block
```css
span {
  display: inline-block;
}
```
It's an `inline` element on steroid. It will respect `margin` and `padding` as
if it's a `block` element but sits next to each other horizontally. Pretty neat!


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

## Manipulate An Element's Position
We can get an element out of its flow. What does that mean?

Well, normally, an element stacks next to each other either
horizontally or vertically as it's written but somehow you want to make
it sticks on top as you scroll down. How? Worry not! We have
`position` property.

There are 5 possible values. These explanations stolen from [w3schools.com](https://www.w3schools.com/css/css_positioning.asp):
* HTML elements are positioned `static` by default
* An element with `position: relative;` is positioned relative to its normal position
* An element with `position: absolute;` is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like `fixed`)
* An element with `position: fixed`; is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled. The `top`, `right`, `bottom`, and `left` properties are used to position the element
* An element with position: sticky; is positioned based on the user's scroll position
