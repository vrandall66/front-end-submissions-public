## Robbie Greiner
Sorting Suite comments

### Testing
* Most of these sorts can handle much larger arrays. Each test only runs 1000 numbers at most.
* Part of the goal of the tests is so you can see the varying efficiency of each sort method.
* Merge and quick in particular can handle tens of thousands of numbers, even in the 2 seconds allotted by mocha

### Bubble
* Since you're using `const` to declare your arrow function, you can export like this: `export default const bubbleSort = `

### Insertion
* Nice use of destructuring

### Merge
* Those `var`s can be `let`s instead
* Good optimization [here](https://github.com/robbiegreiner/sorting-suite/blob/b7438719f2923bf9955d303d560e717ee014a91b/scripts/mergeSort.js#L24)

### Quick
* Oh no! We forgot how to do ES6 suddenly!
* For your own edification, refactor this into ES6.

## Score:
Pass
