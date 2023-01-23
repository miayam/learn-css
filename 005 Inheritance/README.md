# Inheritance

Some CSS properties inherit their value from their parent, user agent default style,
or local user default style:

* `azimuth`
* `border-collapse`
* `border-spacing`
* `caption-side`
* `color`
* `cursor`
* `direction`
* `empty-cells`
* `font-family`
* `font-size`
* `font-style`
* `font-variant`
* `font-weight`
* `font`
* `letter-spacing`
* `line-height`
* `list-style-image`
* `list-style-position`
* `list-style-type`
* `list-style`
* `orphans`
* `quotes`
* `text-align`
* `text-indent`
* `text-transform`
* `white-space`
* `widows`
* `word-spacing`

Let's say:

```html
<html>
  <body>
    <h1>Title</h1>
    <p>I am a robot!</p>
  </body>
</html>
```

```css
* {
  color: blue;
}
```

It will make all elements color blue by default.

For non inheritable properties like `margin` or `padding`, they get initial value
from user-agent base style or local user style (OS, browser extension). They 
didn't inherit it from their parent.

Let's say:

```html
<main>
  <h1>Paragraph</h1>
</main>
```

```css
main {
  margin: 20px;
}
```

`margin: 20px;` that apply to `main` doesn't make `h1` has a margin of 20px.

## How To Explicitly Inherit And Control Inheritance

### Inherit keyword.

```html
<p>
  <strong>I am strong!</strong> <!-- font-weight: 900; -->
<p>
<div>
  <strong>I am not strong enough!</strong> <!-- font-weight: 500; -->
</div>
```

```css
strong {
  font-weight: 500; 
}

p {
  font-weight: 900;
} 

p strong {
  font-weight: inherit;
}
```

### Initial keyword

```html
<p>
  <strong>I am strong!</strong> <!-- font-weight: 500; -->
<p>
<div>
  <strong>I am not strong enough!</strong> <!-- font-weight: 500; -->
</div>
```

```css
strong {
  font-weight: 500; 
}

p {
  font-weight: 900;
} 

p strong {
  font-weight: initial;
}
```

### Unset keyword

```html
<p>
  <strong>I am strong!</strong> <!-- font-weight: 900; -->
<p>
<div>
  <strong>I am not strong enough!</strong> <!-- font-weight: 500; -->
</div>
```

```css
strong {
  font-weight: 500; 
}

p {
  font-weight: 900;
} 

p strong {
  font-weight: unset;
}
```
