# Complete Me
### Student Name: Tom
### Evaluator: Nathaniel Foster

Comments:
* Insert: instead of setting letter to the letter at index 0, you could shift off the first letter. That way you would not need to shift later.
* The return at the end of insert is not doing anything for you. A function automatically returns at the end of a function.
* Take advantage of arrow functions shorthand
```
suggestions.map(word => {
  word = word.name;
  return word;
});
```
---->
`suggestions.map(word => word.name);`

## 1. Process

3: Developer has strategies for approaching complex challenges. Can explain thought process and strategy when prompted.

## 2. Fundamental JavaScript & Style

3: Application shows strong effort towards organization, content, and refactoring

## 3. Test-Driven Development & Code Sanitation

3: Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. Linting shows five or fewer complaints.

## 4. Functional Expectations

4: Application meets all requirements, and implements one extension properly.
