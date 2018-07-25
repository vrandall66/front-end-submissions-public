# Complete Me
### Student Name: Brandon
### Evaluator: Brittany

Comments:
* Problem-solving process was on either end of an extreme -- either too vague and high-level, skipping over details and not providing enough insight, or too low-level and reliant on code for explanations.
* Testing needs to be much more thorough in the future, thinking about edge cases and fleshing out the easier gimmie tests will take you a long way

## 1. Process

2: Developer demonstrates a haphazard, trial and error approach, without clear strategy. Developer does not articulate thought process clearly, and cannot explain the problem-solving strategies they utilized.

## 2. Fundamental JavaScript & Style

3: Application shows strong effort towards organization, content, and refactoring

* [data](https://github.com/brandonfiebiger/complete-me/blob/master/lib/Node.js#L3) I would probably rename 'children' to be a bit more explicit

* Your node instances should probably take in null (for things like this root [node](https://github.com/brandonfiebiger/complete-me/blob/master/lib/Trie.js#L6)), or at least fallback to null if no letter is provided

* You probably don't need to store [suggestions](https://github.com/brandonfiebiger/complete-me/blob/master/lib/Trie.js#L7) as an instance property. This can be a standalone array that exists solely within the suggest method, and is thrown away after each invocation of suggest. There's not really any benefit of holding onto it as an instance property if it's just going to be reset every time suggest is called.

* [This](https://github.com/brandonfiebiger/complete-me/blob/master/lib/Trie.js#L16-L23) is a little difficult to read. Whenever you're working with indexes like 0 and 1, you probably want to store those values in variables with semantic names like 'currentLetter' and 'nextLetter' so other developers can more easily recognize what they represent.


## 3. Test-Driven Development & Code Sanitation

1.5: Application makes some use of very few tests, coverage is too spotty to ensure proper functionality.

* No node tests, should have some gimmies in there at least to verify default instance properties.

* Trie tests are very bare - again, write the gimmie tests at the very least. Insert should verify that the proper nodes are being inserted, that no duplicates can be added, etc. Suggest should assert that words that *dont* belong in the suggestion array don't make it in.

## 4. Functional Expectations

3: Application meets all requirements as laid out per the specification.