# Complete Me
### Student Name: Kurt
### Evaluator: Brittany

Comments:
* Lacked a little confidence when presented with a new problem but did very well after talking it through and whiteboarding a bit. Came up with a solid coded out solution after walking through the thought process and responded well to prompting and guidance.


## 1. Process

3: Developer has strategies for approaching complex challenges. Can explain thought process and strategy when prompted.

## 2. Fundamental JavaScript & Style

3: Application shows strong effort towards organization, content, and refactoring

* You're passing in a [currentLetter](https://github.com/kmiller9393/complete-me/blob/master/lib/Trie.js#L17) when instantiating a new Node here, but your Node class doesn't actually take in any [parameters](https://github.com/kmiller9393/complete-me/blob/master/lib/node.js#L2), so this isn't doing anything.

* I'd expect a method of `count` to simply return the count, not actually modify it. If you want to increment it [here](https://github.com/kmiller9393/complete-me/blob/master/lib/Trie.js#L32-L34) I'd rename it to `incrementCounter`, though I don't think it's worth having this functionality as it's own separate method.

* Rename [this](https://github.com/kmiller9393/complete-me/blob/master/lib/Trie.js#L49) to something more explicity like `suggestions`

## 3. Test-Driven Development & Code Sanitation

4: Application is broken into components which are well tested in both isolation and integration using appropriate data. Linting shows 0 complaints.
3: Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. Linting shows five or fewer complaints.
2: Application makes some use of tests, but the coverage is insufficient. Linting shows ten or fewer complaints.
1: Application does not demonstrate strong use of TDD. Linting shows more than ten complaints.

* What is [this](https://github.com/kmiller9393/complete-me/blob/master/test/Trie-test.js#L5)?

* Insert should also test that nothing is inserted if you try to add a duplicate word

* You might want an initial assertion [here](https://github.com/kmiller9393/complete-me/blob/master/test/Trie-test.js#L47) that verifies the count starts at 0 then equals 2 after the inserts are called.

## 4. Functional Expectations

3: Application meets all requirements as laid out per the specification.