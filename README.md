# PurgeCSS removes necessary Tailwind CSS classes

This repository demonstrates an uncommon bug where PurgeCSS, a tool used to optimize Tailwind CSS builds by removing unused styles, incorrectly removes necessary classes. This can lead to unexpected styling issues in your application.  The bug is demonstrated in `bug.js`. A solution is provided in `bugSolution.js`.

## Bug Description

The issue occurs when certain dynamic class names or edge cases are not properly handled by PurgeCSS.  This results in the removal of classes that are actually needed, breaking the application's styling.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install` to install the necessary dependencies.
3. Run `npm run build` to build the application.
4. Observe the resulting CSS and rendered HTML to see the missing styles.

## Solution

The solution involves carefully configuring PurgeCSS to correctly identify and retain the necessary classes. This might involve adjusting the `content` option in your PurgeCSS configuration to include specific sources or using more sophisticated pattern matching to handle dynamic classes.