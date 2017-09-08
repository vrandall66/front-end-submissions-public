## Lola
Sorting Suite comments

### Testing
* Great use of `import`
* I like that you're putting your test helpers into a single helper file
* The for loop to create assertions is great!
    - Good job balancing when to use it (i.e. not using the loop for testing arrays of 2 or fewer numbers)
* **Love** that you tested your random array generator functions!

### Bubble
* Great use of ES6
* The `export default` can go right before the function declaration:
    - `export default const bubbleSort = `...
* GREAT bundling of your sorts into an `index.js` file!

### Insertion
* See feedback for Bubble

### Merge
* Try refactoring this into ES6 (don't need to do it for a score, just for your own edification)
* [These](https://github.com/lolakoala/sorting-suite/blob/cb126792823a01eeac23f724bdad34123d38d60f/scripts/merge.js#L5-L7) `let`s can be turned into `const`s without damaging your sort
* `newArr.push(ar1[0]); ar1.shift();` can be turned into `newArrpush(ar1.shift())`
    - since `ar1.shift()` returns that value :)

### Quick
* Nice inline solution
* Again, try refactoring into ES6 for the practice
* The solution from your eval is good too!

## Score:
Pass
