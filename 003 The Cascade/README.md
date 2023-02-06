# The Cascade
The cascade is the algorithm for solving conflicts where
multiple CSS rules apply to an element or a group of elements.

The cascade algorithm is split into 4 distinct stages:

1. Position and order of appearance.
2. Specificity.
3. Origin.
4. Importance.

Let's say I author CSS rules in `<style>` tag inside the `<body>` and `<link>` a 3rd party
CSS inside the `<head>`. How does the cascade algorithm work to solve the conflicts?

## Position And Order Of Appearance
If CSS rules in `<style>` and 3rd party CSS have same specificity, then CSS I author
will apply.

## Specificity
If the specificity of CSS rules in `<link>` are bigger than in `<style>` tag, the 3rd party CSS will
apply despite the order of appearance.

## Origin
The cascade takes into account the origin of the CSS: 

1. User agent base styles. Default style from browser makers (Firefox, Chrome, etc).
2. Local user style. Styling from browser extension or OS.
3. Authored CSS. The CSS that we author.
4. Local user style with `!important`.
5. User agent base styles with `!important`.

## Importance
The order of importance of CSS rules:

1. Normal CSS rule such as:

```css
p {
  font-size: 20px;
  background: blue;
  color: red;
}
```

2. `animation` rule type:

```css
/* The animation code stolen from w3schools */
@keyframes example {
  0%   {background-color: red;}
  25%  {background-color: yellow;}
  50%  {background-color: blue;}
  100% {background-color: green;}
}

/* The element to apply the animation to */
div {
  animation-name: example;
  animation-duration: 4s;
}
```

3. `!important` rule type. This is how we do CSS :laughing::

```css
div {
  border-radius: 50% !important;
}
```

4. `transition` rule type.

```css
div {
  width: 100px;
  height: 100px;
  background: red;
  transition: width 2s;
}

div:hover {
  width: 300px; /* The transition will take place when users hover over it. */
}
```
