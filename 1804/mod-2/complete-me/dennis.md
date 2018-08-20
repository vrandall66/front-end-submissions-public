# Complete Me
### Student Name: Dennis
### Evaluator: Brittany

Comments:
* Fine articulation and ability to think through a problem, responded to prompting but needed a bit more than we'd like. Little more practice will solidify this. 


## 1. Process

2.75: Developer has strategies for approaching complex challenges. Can explain thought process and strategy when prompted but might need a bit more guidance than expected.

## 2. Fundamental JavaScript & Style

3: Application shows strong effort towards organization, content, and refactoring

* You're passing in a [currentLetter](https://github.com/dmiller1623/complete-me/blob/master/lib/Trie.js#L16) when instantiating a new Node here, but your Node class doesn't actually take in any [parameters](https://github.com/dmiller1623/complete-me/blob/master/lib/Node.js#L2), so this isn't doing anything.

* This is some really extreme and bizarre [indentation](https://github.com/dmiller1623/complete-me/blob/master/lib/Trie.js#L18)

* This [function](https://github.com/dmiller1623/complete-me/blob/master/lib/Trie.js#L49-L62) should be moved outside to its own method, keeping it within the suggest method makes it much more difficult to test in isolation


## 3. Test-Driven Development & Code Sanitation

2: Application makes some use of tests, but the coverage is insufficient. Linting shows ten or fewer complaints.

* Indentation is also really bizarre in this entire [file](https://github.com/dmiller1623/complete-me/blob/master/test/Trie-test.js)

* Insert method has no tests, and tests are really sparse for suggest. I'd like to see that `getWords` method broken out and tested as well

## 4. Functional Expectations

3: Application meets all requirements as laid out per the specification.
