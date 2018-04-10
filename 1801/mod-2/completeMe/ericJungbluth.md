# Complete Me
### Student Name: Eric Jungbluth
### Evaluator: Cody Sehl

Comments:
* lots of tests - could be good thing, but make sure you're not testing the same thing twice
* first two tests in for insert are testing the same thing
* good empty-case/null-case tests
* `wordCount` property should be `count()` method
* good use of default params on `insert`
* good decomposition

## 1. Process

- Whiteboard adding words
  - jumped right in, lots of confidence
  - good use of vocab
- Whiteboard suggest
  - caught immediately when he started to go somewhere that dind't make sense
  - the only person to decompose `findNode`, `getAllWords(node, prefix)` into separate problems
  - good intuition around what level of detail is adequate for whiteboarding
- Whiteboard a new method `select`
  - good check for empty case
  - good use of vocab
  - stored favorites in the 'root' Node. Might run into problems with that, but confident he could do it
- Write tests for `select`
- Implement `select`

4: Developer demonstrates a clear understanding of their own problem solving process. Logically breaks down large problems into manageable challenges. Has a thoughtful, refined strategy for approaching complex challenges. Developer clearly articulates thought processes.

## 2. Fundamental JavaScript & Style

4: Application demonstrates excellent knowledge of JavaScript syntax, style, and refactoring
3: Application shows strong effort towards organization, content, and refactoring

## 3. Test-Driven Development & Code Sanitation

4: Application is broken into components which are well tested in both isolation and integration using appropriate data. Linting shows 0 complaints.
3: Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. Linting shows five or fewer complaints.

## 4. Functional Expectations

4: Application meets all requirements, and implements one extension properly.
