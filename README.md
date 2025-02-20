# CSS Specificity Bug

This repository demonstrates a subtle bug related to CSS selector specificity.  The bug occurs because a more specific selector overrides a less specific selector, even when the less specific selector is declared later in the stylesheet.

## Bug Description

The bug is demonstrated in the `bug.css` file.  The intended behavior is for all `<p>` elements to have the color red. However, due to the higher specificity of the `div p` selector, the `<p>` elements inside a `<div>` end up having the color blue.

## Solution

The solution is presented in `bugSolution.css`. It uses the `!important` flag to explicitly override the specificity of the `div p` selector. While not ideal in many situations, it helps solve the issue for demonstrating the bug fix.  A better approach would be to refactor the CSS to improve readability and reduce specificity conflicts.