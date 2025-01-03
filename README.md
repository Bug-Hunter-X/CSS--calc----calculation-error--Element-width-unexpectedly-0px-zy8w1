# CSS `calc()` Calculation Error

This repository demonstrates a common issue encountered when using the `calc()` function in CSS.  The problem arises when calculating a dimension (like width or height) based on the size of a parent element that hasn't fully rendered yet.  This frequently leads to the element having an unexpected width of 0px.

The `bug.css` file shows the erroneous code.  The `bugSolution.css` file provides a solution.

## Reproduction

1. Clone the repository.
2. Open `index.html` in your web browser.
3. Observe that the element has an unexpected width of 0px due to the incorrect usage of `calc()`.

## Solution

The solution involves ensuring the parent element's dimensions are known before calculating the child element's dimensions.  This might involve using JavaScript to adjust the child's dimensions after the parent element has rendered, using CSS viewport units, or restructuring the CSS to avoid the dependence on the parent's unknown dimensions.