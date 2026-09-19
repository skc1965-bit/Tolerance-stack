# Tolerance Stack Calculator

A zero-dependency HTML application for linear tolerance stack calculations.

## Features

- Add, edit, subtract, and remove stack contributors
- Worst-case minimum, maximum, and total range
- Statistical root-sum-square (RSS) tolerance estimate
- Optional target/requirement check
- Unit labels, configurable decimal places, example data, and print/PDF support
- Responsive layout with no build step or external dependencies

## Run locally

Open `index.html` in a browser. The app is entirely client-side and can also be hosted directly with GitHub Pages.

## Calculation model

For each contributor, the signed nominal is added to the stack. Tolerance is treated as an absolute value:

- Worst case: `stack nominal ± Σ |tolerance|`
- RSS: `± √(Σ tolerance²)`

RSS assumes independent contributors and is a statistical estimate, not a guaranteed bound.
