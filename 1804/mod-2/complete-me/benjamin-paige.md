# Complete Me
### Student Name: Benjamin Paige
### Evaluator: Pamela Lovett

Comments:
* Struggles with whiteboarding process without reverting back to code. Had to be reminded several times to not write code on whiteboard. Will improve with practice

## 1. Process

3: Developer has strategies for approaching complex challenges. Can explain thought process and strategy when prompted.

## 2. Fundamental JavaScript & Style

3: Application shows strong effort towards organization, content, and refactoring

- `setPref` method in Node is never used? Setting a method of `setWordEnd` seems unecessary to toggle boolean. This method is invoked only once in your functionality.


## 3. Test-Driven Development & Code Sanitation

3: Linting shows 0 complaints. Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. 

- ESLint shows no errors - good job
- Be sure to create new `describe` blocks to encapsulate your `it` testing blocks when testing new methods/different functionality. 
- Testing for `insert` could be more verbose - only testing for instering a single word - testing for multiple words and proper insertion of said words would be better.

## 4. Functional Expectations

4: Application meets all requirements, and implements one extension properly.

- `Delete` implemented with one test. Would like to testing for delete with multiple words in trie

