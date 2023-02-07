# Sizing Units

Have you seen `em`, `rem`, `px`, `deg` somewhere in your CSS code?
Yeah, they are called unit. They are like a system of measurement in physics (`m`, `kg`, `mol`, `A`, etc).
To correctly measure the distance between two elements or the size of the text or the lightness of the color
or the width of an element on the page, we need sizing units to describe them.

If you ask ChatGPT, it says:
> In CSS, sizing units are used to describe the dimensions of elements on a web page such as width, height, font size, and margins. Some common sizing units are pixels (`px`), ems (`em`), rems (`rem`), and percentage (`%`). Pixels are fixed and stay the same size no matter the screen size. Ems and rems change size based on the font size of the parent or root element. Percentage is based on the size of the parent element. The best sizing unit to use depends on the design needs of the web page and the balance between consistency and flexibility.

## Numbers Only
```css
p {
  font-size: 14px;
  line-height: 1.5; /* It's 21px. */
}
```

## Percentage
```css
p {
  color: rgba(0, 0, 0, 50%); /* 50% transparancy. */
}
```

## Degree
```css
p {
  transform: rotate(20deg); /* Rotate 20 degree .*/
}
```

## Dimmensions And Lengths

### Absolute Lengths
There are many absolute length units you can choose from.
Acknowledge them and forget them. The next 100 years,
people will only use `px`.

* `cm` - Centimeters (`96px`/2.54)
* `mm` - Milimeters (1/10 of `1cm`)
* `Q` - Quarter-mimileters (1/40 of `1cm`)
* `in` - Inches
* `pc` - Picas (1/6 of `1in`)
* `px` - Pixels

### Relative Lengths
Some of them are useless and esoteric. I only care about `em`, `rem`, `vw`, and `vh`. You should too.

#### Font-size Relative Units
* `em` - Relative to the font size of the parent element
* `rem` - Relative to the font size of root element (`<html></html>`)

Acknowledge and forget `ex`, `cap`, `ch`, `ic`, `lh`, `rlh`.

#### Viewport Relative Units
* `vw` - 1% of viewport's width
* `vh` - 1% of viewport's height

Acknowledge and forget `vi`, `vb`, `vmin`, and `vmax`.
