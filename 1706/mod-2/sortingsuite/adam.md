## Adam Mescher
Sorting Suite comments

### Testing
* Nice tests
* Instead of using timeout to force each test to run 10000, I would rather see different array lengths
* Part of the point of the testing suite was for you to see the varying efficiencies of the different sorts

### Bubble
* For your own benefit, try refactoring these into ES6
    - `export default`
    - `const`
    - arrow functions
* Good use of destructuring

### Insertion
* See feedback for Bubble

### Merge
* The `let`s can be `const`s since they're not being mutated.
* In the merge function, the second two while loops can be refactored into `result.push(...right, ...left)`

### Quick
* The pivot can be `array.pop()` - then you don't have to worry about accidentally iterating over it in the for loop
    - If you do that, the for loop must be changed to include `i < array.length`

## Score:
Pass
