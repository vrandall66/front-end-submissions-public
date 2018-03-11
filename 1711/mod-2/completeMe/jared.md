## Complete Me Scores
### Student: Jared

### Evaluator:
Brittany

### Evaluator comments: Rely a bit more heavily on your linter and maybe add a couple of rules to your eslint file that enforces strict spacing/line break restrictions. You're logic is nice and concise and easy to follow, but the little stylistic inconsistencies take away from that a bit.


### 1. Fundamental JavaScript & Style

* 3:  Application shows strong effort towards organization, content, and refactoring

* In general, I don't love when variables/property names are called "[data](https://github.com/jaredeklin/complete-me/blob/master/lib/Node.js#L3)" - it's a little too generic to give me any meaningful information

* Look into ES6 getters and setters for [this](https://github.com/jaredeklin/complete-me/blob/master/lib/Trie.js#L9-L11) functionality. Classes can essentially have a get and/or set method that can be used for retrieving these types of values

* [Meh ugly space in your while condition here](https://github.com/jaredeklin/complete-me/blob/master/lib/Trie.js#L17) and [random blank line here](https://github.com/jaredeklin/complete-me/blob/master/lib/Trie.js#L35). Little nitpicky things like this make a difference ;)

* [This](https://github.com/jaredeklin/complete-me/blob/master/lib/Trie.js#L77-L79) is a nice place for using that implicit return so the logic can all be done on a single line


### 2. Test-Driven Development

* 3: Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality

### 3. Encapsulation / Breaking Logic into Components

* 3: Application effectively breaks logical components apart but breaks the principle of SRP

### 4. Functional Expectations

* 3: Application meets all requirements as laid out per the specification.
