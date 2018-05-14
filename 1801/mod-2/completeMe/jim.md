# Complete Me
### Student Name: Jim
### Evaluator: Brittany

Comments:
* [This test](https://github.com/Ecksi/complete-me/blob/master/tests/Trie-test.js#L46-L55) is kind of redundant/unecessary. There's really nothing special about adding four words as opposed to one or two or three.
* You probably don't need to store your [suggesstions](https://github.com/Ecksi/complete-me/blob/master/scripts/Trie.js#L7-L8) as an instance property on the Trie -- just have the suggest method create this array and return it each time the method is called, you won't need to hold onto that value for any longer than the duration of the method execution
* An edge case to test [here](https://github.com/Ecksi/complete-me/blob/master/tests/Trie-test.js#L107) with suggest is to also insert a word that wouldn't match the prefix, and assert that it *doesn't* get included in the suggestions array

## 1. Process

3: Developer has strategies for approaching complex challenges. Can explain thought process and strategy when prompted.

## 2. Fundamental JavaScript & Style

3: Application shows strong effort towards organization, content, and refactoring

## 3. Test-Driven Development & Code Sanitation

3: Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. Linting shows five or fewer complaints.

## 4. Functional Expectations

4: Application meets all requirements, and implements one extension properly.