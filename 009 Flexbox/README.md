# Flexbox

## Axis
![axis](./main-and-cross-axis.svg)

### What is main axis? 
The main axis is the one set by `flex-direction` property. If that is `row` your main axis is along the `row`, if it is `column` your main axis is along the `column`. 

### What is cross axis?
The cross axis runs in the other direction to the main axis, so if `flex-direction` is `row` the cross axis runs along the `column`.

## What is `flex-flow`?
A shorthand for `flex-direction` and `flex-wrap`.

```
p {
  flex-flow: row wrap;
}

p {
  flex-direction: row;
  flex-wrap: wrap;
}
```

## What would happen if we set `flex` to `initial`?

## What would happen if we set `flex` to `auto`?

## What would happen if we set `flex` to  `1`?
