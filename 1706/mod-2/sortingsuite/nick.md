## Nick Teets
Sorting Suite comments

### Testing
* [I like that you pulled out the random array generators into a separate helper file](https://github.com/nicktu12/sorting-suite/blob/51291bac32292875bf6c537591d32519e7d97ff6/tests/bubble-sort-test.js#L3)
* It's probably better for [this](https://github.com/nicktu12/sorting-suite/blob/51291bac32292875bf6c537591d32519e7d97ff6/tests/bubble-sort-test.js#L11-L18) test's assert to read like
  
    - I like how you're testing with the larger arrays, with a for loop, but for an array of one, it's better to be explicit since you know exactly what the output is supposed to be.
    - The same goes for sorting an array of 2 numbers.
    - The for loop is a bit heavy for these particular tests.
* The same comments apply to the other test suites :)
* The for loop assertion is very good! Great implementation.

### Bubble
* The inner for loop is using var instead of let :(

### Insertion
* The inner for loop is using var instead of let here, too :(

### Merge
* Change those vars to lets!
* [This is a great optimization](https://github.com/nicktu12/sorting-suite/blob/51291bac32292875bf6c537591d32519e7d97ff6/scripts/merge-sort.js#L19)

### Quick
* The pivot can just be 
    - That way, you don't have to worry about your for loop ending at 
    - By popping the pivot off the array, you never run the risk of iterating over it and getting trapped in the loop forever
* Nice use of the spread operator in your return

## Score:
Pass
