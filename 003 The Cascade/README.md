# The Cascade
The cascade is the algorithm for solving conflicts where
multiple CSS rules apply to an element or a group of elements.

The cascade algorithm is split into 4 distinct stages:

1. Position and order of appearance.
2. Specificity.
3. Origin.
4. Importance.

Let's say I author CSS rules in `<style>` tag inside the `body` and link a 3rd party
CSS inside the `head`. How does the cascade algorithm work to solve the conflicts?

## Position And Order Of Appearance
If CSS rules in `<style>` and 3rd party CSS have same specificity, then CSS I author
will apply.

## Specificity
If the specificity of CSS rules in `<link>` are bigger than in `<style>` tag, the 3rd party CSS will
apply despite the order of appearance.

## Origin
The cascade takes into account the origin of the CSS. The order of specificity of these origins, from least specific, to most specific is as follows:

1. User agent base styles. Default style from browser makers (Firefox, Chrome, etc).
2. Local user style. Styling from browser extension or OS.
3. Authored CSS. The CSS that we author.
4. Local user style with `!important`.
5. User agent base styles with `!important`.

## Importance
The order of importance, from least important, to most important is as follows:

1. Normal rule type, such as `font-size`, `background` or `color`.
2. `animation` rule type.
3. `!important` rule type (following the same order as origin).
4. `transition` rule type.
