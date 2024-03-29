# Selectors

How do you apply styling to an element or a group of elements on the web page?
> We search for an element or a group of elements with CSS selector and write CSS description that reflects the styling.

What is CSS selector?
> A token to find a specific element or a group of elements and apply styling to it.

What is CSS description?
> A pair of property and value that describes what styling we are going to apply.

What is CSS rule?
> A piece of code that consist of CSS selector and CSS description.

We group selectors in 3 section (simple selectors, pseudo selectors, complex selectors). 

## Simple Selectors

```css
* { /* CSS selector (universal selector) */
  box-sizing: border-box; /* CSS description */
}

section { /* CSS selector (type selector) */
  padding: 2em;  /* CSS description */
}

.selector { /* CSS selector (class selector) */
  color: lightblue; /* CSS description */
}

#selector { /* CSS selector (id selector) */
  margin: 1em; /* CSS description */
}

[href='https://web.dev'] { /* CSS selector (attribute selector) */
  line-height: 1em; /* CSS description */
}

[href*='example.com'] { /* CSS selector (attribute selector). A href that contains "example.com" */
  color: red; /* CSS description */
}

/* CSS rule */
[href^='https'] { /* CSS selector (attribute selector). A href that starts with https */
  color: green; /* CSS description */
}

/* CSS rule */
[href$='.com'] { /* CSS selector (attribute selector). A href that ends with .com */
  color: blue; /* CSS description */
}

```

## Pseudo Selectors
```css
p::before,
p::after { /* CSS selector (pseudo-element selector). A CSS pseudo-element is used to style specified parts of an element.
 */
  margin-left: 2px; /* CSS description */
}

p:hover,
p:focus { /* CSS selector (pseudo-class selector). A pseudo-class is used to define a special state of an element.
 */
  border-radius: 50%; /* CSS description */
}
```

## Complex Selectors
```css
main p { /* CSS selector (descendant, all p inside main) */
  position: absolute; /* CSS description */
}

p + p { /* CSS selector (adjuscent sibling) */
  transform: translateX(-50%); /* CSS description */
}

h2 ~ p { /* CSS selector (general sibling) */
  background-color: blue; /* CSS description */
}

main > p { /* CSS selector (direct child) */
  display: flex; /* CSS description */
}

p.selector.selector1 { /* CSS selector (compound to increase specificity) */
  margin-right: 300px; /* CSS description */
}
```

What is the difference between `~` and `+` ?

Let's say we'd like to have the vertical gap of 20px between each paragraph and all paragraphs that follows with `<h2>` must be red.

```html
<main>
  <h1>Title 1</h1>
  <p>
    Paragraph 1 <!-- Nothing applies to this paragraph. -->
  </p>
  <p>
    Paragraph 2 <!-- Margin top of 20px. -->
  </p>
  <div>
    Woops
  </div>
  <p>
    Paragraph 3 <!-- Nothing applies to this paragraph. -->
  </p>
  <p>
    Paragraph 4 <!-- Margin top of 20px. -->
  </p>
  <h1>Title 2</h1>
  <p>
    Paragraph 5 <!-- Nothing applies to this paragraph. -->
  <p>
  <p>
    Paragraph 6 <!-- Margin top of 20px. -->
  <p> 
  <h2>Sub title for title 2</h2>
  <p>
    Paragraph 7 <!-- Red text. -->
  </p>
  <div>
    Woops
  </div>
  <p>
    Paragraph 8 <!-- Red text. -->
  </p>
  <p>
    Paragraph 9 <!-- Red text. Margin top of 20px. -->
  </p>
</main>
```

Here's how it's done:
```css
main > p + p {
  margin-top: 20px;
} 

main > h2 ~ p {
  color: red;
}
```

See the difference?
