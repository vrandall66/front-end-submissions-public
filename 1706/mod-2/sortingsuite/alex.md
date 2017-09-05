## Alex Banister
Sorting Suite comments

### Testing
* I like that you pulled in the random array generators from a separate helper file
* Was 5000 the longest length array you could run merge sort on in the 2 seconds allotted during tests?
* With merge and quick sorts, I'd like to see the random arrays being sorted have lengths of ten thousands.

### Bubble
* Since we're not using `this`, I'd like to see ES6 here.
* Nice optimization using the "sorted" boolean
* In your inner for loop, you have `i < (toSort.length - 1)`; you don't need the parentheses there :)

### Insertion
* Make friends with arrow functions :)
* Instead of using `} else { break; }`, you can just leave out the else statement.

### Merge
* Try for a `const mergeSort = (array) => {` format here

### Quick
* If you use ES6, you can export by writing `export default const [FUNCTION NAME] = (array) => {}`
* Nice use of the spread operator in your return

## Score:
Pass
