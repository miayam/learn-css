# Selectors

How do you apply styling to an element or a group of elements on the web page?
> We search for an element or a group of elements with CSS selector and write CSS description that reflects the styling.

What is CSS selector?
> A token to find a specific element or a group of elements and apply CSS rule to it.

What is CSS description?
> A pair of property and value that describes what styling we are going to apply.

What is CSS rule?
> A piece of code that consist of one or many CSS selectors and one or many CSS descriptions.

We group selectors in 3 section (simple selectors, pseudo selectors, complex selectors). 

## Simple Selectors

```css
/* CSS rule */
* { /* CSS selector (universal selector) */
  box-sizing: border-box; /* CSS description */
}

/* CSS rule */
section { /* CSS selector (type selector) */
  padding: 2em;  /* CSS description */
}

/* CSS rule */
.selector { /* CSS selector (class selector) */
  color: lightblue; /* CSS description */
}

/* CSS rule */
#selector { /* CSS selector (id selector) */
  margin: 1em; /* CSS description */
}

/* CSS rule */
[href='https://web.dev'] { /* CSS selector (attribute selector) */
  line-height: 1em; /* CSS description */
}
```

## Pseudo Selectors
```css
/* CSS rule */
p::before,
p::after { /* CSS selector (pseudo-element selector). A CSS pseudo-element is used to style specified parts of an element.
 */
  margin-left: 2px; /* CSS description */
}

/* CSS rule */
p:hover,
p:focus { /* CSS selector (pseudo-class selector). A pseudo-class is used to define a special state of an element.
 */
  border-radius: 50%; /* CSS description */
}
```

## Complex Selectors
```css
/* CSS rule */
main p { /* CSS selector (descendant, all p inside main) */
  position: absolute; /* CSS description */
}

/* CSS rule */
p + p { /* CSS selector (adjuscent sibling) */
  transform: translateX(-50%); /* CSS description */
}

/* CSS rule */
h2 ~ p { /* CSS selector (general sibling) */
  background-color: blue; /* CSS description */
}

/* CSS rule */
main > p { /* CSS selector (direct child) */
  display: flex; /* CSS description */
}

/* CSS rule */
p.selector.selector1 { /* CSS selector (compound to increase specificity) */
  margin-right: 300px; /* CSS description */
}
```

The difference between `~` and `+` ?

Let's say we have HTML code:

```html
<main>
  <h1>Title 1</h1>
  <p>
    Paragraph 1 <!-- p + p will apply to this paragraph. -->
  </p>
  <p>
    Paragraph 2 <!-- p + p will apply to this paragraph. -->
  </p>
  <h1>Title 2</h1>
  <p>
    Paragraph 4 <!-- h2 ~ p won't apply to this paragraph. p + p will apply to this paragraph. -->
  <p>
  <p>
    Paragraph 5 <!-- h2 ~ p won't apply to this paragraph. p + p will apply to this paragraph. -->
  <p> 
  <h2>Sub title for title 2</h2>
  <p>
    Paragraph 6 <!-- h2 ~ p will apply to this paragraph. p + p will apply to this paragraph. -->
  </p>
  <p>
    Paragraph 7 <!-- h2 ~ p will apply to this paragraph. p + p will apply to this paragraph. -->
  </p>
</main>
```

We'd like to have the vertical gap of 20px between each paragraph and all paragraphs that follows with `<h2>` must be red. How?

```css
main > p + p {
  margin-top: 20px;
} 

main > h2 ~ p {
  color: red;
}
```
See the difference?

