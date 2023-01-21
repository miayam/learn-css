# Specificity

Universal selector (`*`) = 0.

Type selector (`a`, `button`, `section`, etc) = 1.

Pseudo-element selector (`::before`, `::selection`, `::marker`, etc) = 1.

Class selector (`.className`) = 100.

Attribute selector (`[href='https://web.dev']) = 100.

Pseudo-class selector (`:hover`, `:focus`, etc) = 100.

Id selector (`#id`) = 1000.

`!important` = 10000.