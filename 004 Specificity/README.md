# Specificity

Universal selector (`*`) = 0.

Type selector (`a`, `button`, `section`, etc) = 1.

Pseudo-element selector (`::before`, `::selection`, `::marker`, etc) = 1.

Class selector (`.className`) = 10.

Attribute selector (`[href='https://web.dev']) = 10.

Pseudo-class selector (`:hover`, `:focus`, etc) = 10.

Id selector (`#id`) = 100.

Inline style attribute = 1000.

`!important` = 10000.