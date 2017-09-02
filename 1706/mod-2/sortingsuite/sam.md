## Samuel Singer
Sorting Suite comments

### Testing
* These sorts can handle HUGE sets of numbers, even in the 2 second constraint of the test suite
* Merge and Quick in particular can handle tens of thousands of numbers
* Part of the point of the tests was seeing how much more efficient some of the sorts are than others

### Bubble
* Good use of ES6
* The `export default` can go right before the function declaration:
    - `export default const bubbleSort = `...
    - instead of using `module.exports`

### Insertion
* See feedback for Bubble

### Merge
* Oh no! Where did our ES6 go?
* Try refactoring this into ES6 (don't need to do it for a score, just for your own edification)
* [These](https://github.com/Cache123/TDD/blob/4dbc2edb775393ac44dd62e9077c09eeb11c202e/scripts/mergeSort.js#L2-L4) `let`s can be turned into `const`s without damaging your sort
* The line you [asked about](https://github.com/Cache123/TDD/blob/4dbc2edb775393ac44dd62e9077c09eeb11c202e/scripts/mergeSort.js#L23) is perfectly fine and is a great optimization.

### Quick
* Again, try refactoring into ES6 for the practice

## Score:
Pass
