## Complete Me Scores
### Student:
Theresa

### Evaluator:
Nathaniel

### Evaluator comments:
* `require('./Trie');` in your index.js is not doing anything for you. 
Either `const Trie = require('./Trie');` or `import Trie from './Trie';`
* In `addWordToTrie`, using an if/else instead of two individual if statements would be better, `if (word.length === 1) {} else if (word.length > 1) {}`. Since only one of these can be true, it would be better to use an if/else.
* In `suggest` your `while` loop is based on a counter so it would be better to use a for loop which is made for doing something a set number of times.
* In your select you can use `Object.hasOwnProperty([propname])` instead of `(Object.keys(currentLevel).find(letter => letter === currentLetter))` to check if an object has a property.
* `expect(completion.suggest('dog')).to.be.a.function;` is not a good test
`expect('').to.be.a.function;` also passes. 

To test if something is a function try doing something like
`expect(completion.suggest).to.be.an.instanceof(Function);`

### 1. Fundamental JavaScript & Style

* 3:  Application shows strong effort towards organization, content, and refactoring

### 2. Test-Driven Development

* 3: Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality

### 3. Encapsulation / Breaking Logic into Components

* 3: Application effectively breaks logical components apart but breaks the principle of SRP

### 4. Functional Expectations

* 3: Application meets all requirements as laid out per the specification.
