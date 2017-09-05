## Jen Woodson
Sorting Suite comments

### Testing
* Great use of `import`
* It would be great to put all your helper functions into one file
    - and use `module.exports = { function1, function2, function3 }`
    - and then `import { function1, function2, function3 } from './helper'`
* The for loop to create assertions is great!
    - It's too heavy, though, for the tests for arrays with 1 or 2 numbers
    - In those cases, just specify the expected arrays
* I'd love to see your merge and quick sort tests really seeing how efficient these sorts are
    - They can handle tens of thousands of numbers, generally

### Bubble
* For your own benefit, try refactoring these into ES6
    - `export default`
    - `const`
    - arrow functions
* Good use of destructuring

### Insertion
* See feedback for Bubble

### Merge
* The base case can be moved to the top of the function
    - Then, we're not needlessly defining the two split arrays and the midpoint :)
    - You don't need the `else` statement; it can just be below the base case and variable declarations
* Turn those `var`s into `let`s
* In the merge function, the last two while loops can be refactored into `result.push(...right, ...left)`

### Quick
* The base case can go at the top of the function so we're not needlessly defining variables
* The pivot can be `array.pop()` - then you don't have to worry about accidentally iterating over it in the for loop
    - If you do that, the for loop must be changed to include `i < array.length`

## Score:
Pass
