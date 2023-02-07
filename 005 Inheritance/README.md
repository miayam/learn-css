# Inheritance

Some CSS properties inherit their value from their parent:

```css
body {
  font-family: Helvetica;
  color: #000;
}

p {
  font-weight: bold;
}
```

```html
<body>
  <p>
    I am Batman!
  </p>
</body>
```

Despite the fact that the CSS rule that applies to it is only `font-weight: bold;`, the paragraph `<p>` will be a bold black
Helvetica. Well, **I am Batman!**

The majority of CSS properties derive their value from the browser's default styling (Chrome, Firefox, Edge, Opera, etc) or the default styling imposed by your OS (Windows, Linux, macOS, etc).

Personally, I am only concerned with `font-size`, `font-family`, `font-weight`, and `color`. Forget some of them if you choose so.

These are inheritable CSS properties:

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

It will make all text blue by default.

For non inheritable properties like `margin` or `padding`, they get initial value
from default styling imposed by your browser or OS. They didn't inherit it from
their parent.

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

`margin: 20px;` that apply to `main` doesn't make `h1` has a margin of `20px`.

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
