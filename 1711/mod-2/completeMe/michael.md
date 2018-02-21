## Complete Me Scores
### Student: Michael

### Evaluator:
Nathaniel

### Evaluator comments:
* You need to require and module.exports your trie in your index.js file
* The check for duplicates in your insert is overly complicated. You can just go about inserting the word and do a check when you get to the final letter in the word. Only increase the word count if there is not a node for the last letter in the word.
* When you have a while loop where the conditional is based on a count, you should just use a for loop since those are built to be used with a count. See your while loop in your suggest function.
* Your populate function will only ever insert 10000 words. You do not need two for loops to accomplish this you can just use one for loop e.g. `for (let i = 0; i < 10000; i++) {}`
* Your `return` in your forEach callback function is not accomplishing anything. See line 102 & 115.
* for some reason your node data property was commented out which meant your first test was not passing.

### 1. Fundamental JavaScript & Style

* 3:  Application shows strong effort towards organization, content, and refactoring

### 2. Test-Driven Development

* 3: Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality

### 3. Encapsulation / Breaking Logic into Components

* 3: Application effectively breaks logical components apart but breaks the principle of SRP

### 4. Functional Expectations

* 3: Application meets all requirements as laid out per the specification.
