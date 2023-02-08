# Color

There are 6 ways to set color in CSS.

## Hexadecimal
```css
p {
  color: #000000; /* It's going to be black. */
}

p {
  color: #aa44ee; /* Purple. */
}
```

You can also write hex codes in a three digit shorthand like this:
```css
p {
  color: #000; /* It's going to be black. */
}

p {
  color: #a4e; /* Purple. */
}
```
How do we adjust transparancy in hexadecimal?

Let's say we want to add 50% transparancy to a black text (`#000000`).
There are 4 slots to place hexadecimal value, each of which has maximum
value of `FF` or 255 in decimal. The last slot is to define transparancy.
What is 50% of 255? It is 127.5 but we round it to 128. We convert 128
into hexadecimal which is `80`. So, the  CSS value to define black with
50% transparancy is `#00000080`. 

## RGB

There are 3 slots. Each of which has maximum value of 255. The forward slash
`/` after 3 sequences of decimal number is to define transparancy (0 - 1 or 0% - 100%).

```css
p {
  color: rgba(0, 0, 0); /* Black. */
}

p {
  color: rgb(0 0 0); /* Black. */
}

p {
  color: rgb(0 0 0 / 0.5); /* Black with 50% transparancy. */
}

p {
  color: rgb(0 0 0 / 50%); /* Black with 50% transparancy. */
}

p {
  color: rgb(0, 0, 0 / 0.5); /* Black with 50% transparancy. */
}

p {
  color: rgb(0, 0, 0 / 50%); /* Black with 50% transparancy. */
}
```

## RGBA
Almost the same as RGB but use slightly different syntax.

```css
p {
  color: rgba(0, 0, 0); /* Black. */
}

p {
  color: rgba(0, 0, 0, 50%); /* Black with 50% transparancy. */
}

p {
  color: rgba(0, 0, 0, 0.5); /* Black with 50% transparancy. */
}
```  

## HSL

Hue, saturation, lightness. Think color wheel in Photoshop.

### Hue
Hue is a degree on the color wheel from 0 to 360. 0 is red, 120 is green, 240 is blue.

### Saturation
Saturation is a percentage value; 0% means a shade of gray and 100% is the full color.

### Lightness
Lightness is also a percentage; 0% is black, 100% is white.

```css
p {
  color: hsl(0, 0%, 0%); /* Black. */
}

p {
  color: hsl(0 0% 0%); /* Black. */
}

p {
  color: hsl(0 0% 0% / 50%); /* Black with 50% transparancy. */
}

p {
  color: hsl(0 0% 0% / 0.5); /* Black with 50% transparancy. */
}

p {
  color: hsl(0deg 0% 0%); /* Black. */
}

p {
  color: hsl(0turn 0% 0%); /* Black. */
}
```

## HSLA
Hue, saturation, lightness, alpha.

### Hue
Hue is a degree on the color wheel from 0 to 360. 0 is red, 120 is green, 240 is blue.

### Saturation
Saturation is a percentage value; 0% means a shade of gray and 100% is the full color.

### Lightness
Lightness is also a percentage; 0% is black, 100% is white.

### Alpha
An optional alpha component represents the color's transparency. 0 - 1 or 0% - 100%.

```css
p {
  color: hsla(0, 0%, 0%); /* Black */
}

p {
  color: hsla(0, 0%, 0%, 50%); /* Black with 50% transparancy. */
}

p {
  color: hsla(0, 0%, 0%, 0.5); /* Black with 50% transparancy. */
}

p {
  color: hsla(0deg, 0%, 0%); /* Black */
}

p {
  color: hsla(0turn, 0%, 0%); /* Black */
}
```

## Color Keywords
There are 148 named colors in CSS. These are plain English names such as `red`, `black`,
`purple`, `tomato` and `goldenrod`. There's no use remembering them.
