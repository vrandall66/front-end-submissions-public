# Complete Me
### Student Name: Kiel
### Evaluator: Brittany

Comments:
* Nice whiteboarding and articulation at a high-level, falls apart a little bit when converting that into code. Seems to have a thought process in place but looses track of it when switching contexts.
* Naming conventions need some work to improve readibility of your code

## 1. Process

2.75: Developer has strategies for approaching complex challenges. Can explain thought process and strategy when prompted but might need a bit more guidance than expected.

## 2. Fundamental JavaScript & Style

4: Application demonstrates excellent knowledge of JavaScript syntax, style, and refactoring
3: Application shows strong effort towards organization, content, and refactoring
2: Application runs but the code has long methods, unnecessary or poorly named variables, and needs significant refactoring
1: Application generates syntax error or crashes during execution

* Child should probably be renamed to [children](https://github.com/kielzor/complete-me/blob/master/lib/node.js#L4) as you can have more than one child per node

* What is [this](https://github.com/kielzor/complete-me/blob/master/lib/trie.js#L1)

* Not a huge fan of your abbreviations [here](https://github.com/kielzor/complete-me/blob/master/lib/trie.js#L11-L12). 'word' would be better than 'val' and 'letters' would be better than 'arr'

* Arrays should be [plural](https://github.com/kielzor/complete-me/blob/master/lib/trie.js#L36) - suggestedWords

## 3. Test-Driven Development & Code Sanitation

3: Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. Linting shows five or fewer complaints.

* I'd rephrase this [it block](https://github.com/kielzor/complete-me/blob/master/test/trie-test.js#L100) to say 'it should not increment when adding a duplicate word'. Otherwise it sounds like a repeat of one of your earlier insert tests

* Nice job testing edge cases like duplicates and words that should not be suggested

## 4. Functional Expectations

3: Application meets all requirements as laid out per the specification.