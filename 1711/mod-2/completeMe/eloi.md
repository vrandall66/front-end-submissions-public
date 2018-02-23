## Complete Me Scores
### Student: Eloi

### Evaluator:
Brittany

### Evaluator comments: Solid logic and approach, code could use a little bit of cleanup and refactoring but overall easy to follow and read.


### 1. Fundamental JavaScript & Style

* 3:  Application shows strong effort towards organization, content, and refactoring

* Node [file name](https://github.com/eloimercado/complete-me/blob/master/lib/node.js) should be capitalized as well, just like you did with Trie.js. Tells us right away it contains a class without us having to dig in and look at the code.

* [This](https://github.com/eloimercado/complete-me/blob/master/lib/Trie.js#L34) is a bit too much logic to put into your if condition. I'd rather see you break this out and store it in a variable so that you can just say `if(variable)` instead of doing all this evaluation in your conditional.

* [This](https://github.com/eloimercado/complete-me/blob/master/lib/Trie.js#L69-L71) logic is simple enough it would be a nice place to use that implicit return by putting it all on one line

* The [suggest](https://github.com/eloimercado/complete-me/blob/master/lib/Trie.js#L41-L66) method is a little overwhelming at first glance. I'd give your code a little more room to breathe here, maybe with just a blank line right before you get into the meat of the logic where you define `searchWords`

### 2. Test-Driven Development

* 3: Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality

### 3. Encapsulation / Breaking Logic into Components

* 3: Application effectively breaks logical components apart but breaks the principle of SRP

### 4. Functional Expectations

* 3: Application meets all requirements as laid out per the specification.
