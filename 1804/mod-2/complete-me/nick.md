# Complete Me
### Student Name: Nick
### Evaluator: Brittany

Comments:
* Thorough thought process and articulation; needed some extra guidance around the coding but overall kept a logical step-by-step process.

## 1. Process

2.75: Developer has strategies for approaching complex challenges. Can explain thought process and strategy when prompted but might need a bit more guidance than expected.

## 2. Fundamental JavaScript & Style

3: Application shows strong effort towards organization, content, and refactoring

* You're passing in a [currentLetter](https://github.com/30ozSteak/complete-me/blob/master/lib/Trie.js#L17) when instantiating a new Node here, but your Node class doesn't actually take in any [parameters](https://github.com/30ozSteak/complete-me/blob/master/lib/Node.js#L2), so this isn't doing anything.

* Using the word [node](https://github.com/30ozSteak/complete-me/blob/master/lib/Trie.js#L47-L49) here as a parameter, and pushing into it seems a little confusing. If this represents your suggestions array, I would rename it to something more explicit like 'suggestions'. node makes me think it represents an instance of the node class.

* Curious what the spread operator is doing for you [here](https://github.com/30ozSteak/complete-me/blob/master/lib/Trie.js#L59), it looks like your insert method just takes in a word on its own and spreads it right away.

* Instead of a `countUp` method, you can look into getters and setters for ES6 classes to create a method that returns that count value for you. It would look something like `get count() { return count }`

## 3. Test-Driven Development & Code Sanitation

3: Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. Linting shows five or fewer complaints.

* Put your suggestion tests in a separate describe block, it's hard to see they exist as their meshed in with your insert tests.

* I'd make an initial assertion [here](https://github.com/30ozSteak/complete-me/blob/master/test/trie-test.js#L96-L99) that ensures the count is 0, then 1, then 0 again after the delete. As this test is written now, it might be that the counter value is never updated and always remains at 0. We want to make sure that it decrements from 1 to 0 after a delete is performed.


## 4. Functional Expectations

4: Application meets all requirements, and implements one extension properly.

* Delete method completed during eval