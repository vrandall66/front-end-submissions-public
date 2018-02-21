## Complete Me Scores
### Student: Sabrina

### Evaluator:
Nathaniel

### Evaluator comments:
* You should import and export your trie in your index file
* In `insert` you can combine your nested if statements.
```
if(currentNode[currentLetter].completeWord === false) {
  if(!lettersArray.length) {
    this.wordCounter++;
    currentNode[currentLetter].completeWord = word;
  }
}
```
to
```
if(currentNode[currentLetter].completeWord === false && !lettersArray.length) {
  this.wordCounter++;
  currentNode[currentLetter].completeWord = word; 
}
```

* To check if an object has a property, try using `Object.hasOwnProperty('propName');` instead of `Object.keys(currentNode).find(letter => letter === currentLetter`
* In your delete, you should check to make sure that a node is a complete word before decrementing the word count.

### 1. Fundamental JavaScript & Style

* 3:  Application shows strong effort towards organization, content, and refactoring

### 2. Test-Driven Development

* 3: Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality

### 3. Encapsulation / Breaking Logic into Components

* 4: Application is expertly divided into logical components each with a clear, single responsibility

### 4. Functional Expectations

* 3: Application meets all requirements as laid out per the specification.
