# Complete Me
### Student Name: Todd
### Evaluator: Brittany/Pam

Comments:
* Difficult time knowing how to get started and very rigid in thought-process, couldn't respond to prompting in a way that would get them on the right path again.

## 1. Process

2: Developer demonstrates a haphazard, trial and error approach, without clear strategy. Developer does not articulate thought process clearly, and cannot explain the problem-solving strategies they utilized.

## 2. Fundamental JavaScript & Style
    
2.5: Application runs but the code has long methods, unnecessary or poorly named variables, and needs refactoring

- The variable name `wordLetters` could be better as just `letters`.
- Line 22 could be `firstLetter` as opposed to just `letter`.

## 3. Test-Driven Development & Code Sanitation

2: Application makes some use of tests, but the coverage is insufficient. Linting shows more than ten complaints.

- ESLint shows 23 problems (9 errors, 14 warnings)
- Remove commented out code from testing suite
- Be sure to create new `describe` blocks to encapsulate your `it` testing blocks when testing new methods/different functionality. 
- No tests present for `populate` or `searchNodes`
- Would like to see more verbose testing for `insert` - testing with multiple words and checking children nodes to be sure trie is building out correctly.

## 4. Functional Expectations

2.75: Application runs, but does not fully meet specifications.

- 1/2 way through Phase III - missing `count` method that returns a count of words inserted (although property of count set and working on `Trie`)