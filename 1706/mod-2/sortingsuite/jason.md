## Jason Hughes
Sorting Suite comments

### Testing
* I'd love to see your tests increment up in complexity
    - Start with an array of 1 number
    - Move to 2 numbers
    - Random array (hundreds)
    - Random array (tens of thousands)
* This will help you see the varying efficiency of each of these sorts

### Bubble
* Good use of ES6
* The `export default` can go right before the function declaration:
    - `export default const bubbleSort = `...
    - instead of using `module.exports`

### Insertion
* See feedback for Bubble

### Merge
* Noooooo where did the ES6 go?
* This is not a requirement, but refactor this into ES6 for your own edification

### Quick
* This is not a requirement, but refactor this into ES6 for your own edification
* The pivot can be `array.pop()`
    - This requires the for loop to specify `i < arr.length`
    - Elminates possibility of comparing it to itself and being trapped in a loop forever
* Remove the `console.log`s and `debugger`s from your production code!

## Score:
Pass
