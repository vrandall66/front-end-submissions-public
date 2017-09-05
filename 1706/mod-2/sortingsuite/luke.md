## Luke Finney
Sorting Suite comments

### Testing
* Try using `import` instead of `require`
* Great scaling of your tests (sorting 10000 with bubble and insertion, and 100000 with merge and quick)

### Bubble
* Good use of ES6
* The `export default` can go right before the function declaration:
    - `export default const bubbleSort = `...
    - instead of using `module.exports`

### Insertion
* See feedback for Bubble

### Merge
* [These](https://github.com/lfinney/sorting-suite-m2/blob/9c3cc4a3aface2b47d819aeb380514ffd43cb1c9/scripts/mergeSort.js#L5-L7) `let`s can be turned into `const`s without damaging your sort
* You `merge` function can use `const` instead of `let`

### Quick
* The pivot can be `array.pop()`
    - This requires the for loop to specify `i < arr.length`
    - Elminates possibility of comparing it to itself and being trapped in a loop forever

## Score:
Pass
