# Complete Me
### Student Name: Daniela
### Evaluator: Brittany

Comments:
* Wonderful articulation and problem-solving process, great confidence and flexibility in understanding
* Nice job testing before and after values in assertions like [this](https://github.com/danielafcarey/TDD/blob/complete-me/tests/Trie-test.js#L33-L35)
* Nice [edge](https://github.com/danielafcarey/TDD/blob/complete-me/tests/Trie-test.js#L81) case [assertions](https://github.com/danielafcarey/TDD/blob/complete-me/tests/Trie-test.js#L49) these are really difficult to anticipate and you nailed all of them
* It looks like you may have updated your code a bit for denoting the end of a word, [this](https://github.com/danielafcarey/TDD/blob/complete-me/tests/Trie-test.js#L66) description doesn't quite match what your code actually does.
* Look into ES6 classes getters and setters for doing something like [this](https://github.com/danielafcarey/TDD/blob/complete-me/scripts/Trie.js#L32-L34). Instead of having a method `count` that returns a property `wordCount`, you can use a getter to return that value directly to the user.
* [This test](https://github.com/danielafcarey/TDD/blob/complete-me/tests/Trie-test.js#L171-L176) is probably a little unecessary/redundant. Your suggest tests should cover this just fine.
* Nice [error handling](https://github.com/danielafcarey/TDD/blob/complete-me/scripts/Trie.js#L14-L17)
* Even though `word.length` works with [strings](https://github.com/danielafcarey/TDD/blob/complete-me/scripts/Trie.js#L19), I might consider still splitting the word out into an array. Generally when you're looping using a length value, you tend to think you're working with an array rather than a string. You won't often see people using the `length` property on strings. It's just a teensy bit confusing/less semantic.
* You probably don't need to store your [suggesstions](https://github.com/danielafcarey/TDD/blob/complete-me/scripts/Trie.js#L7) as an instance property on the Trie -- just have the suggest method create this array and return it each time the method is called, you won't need to hold onto that value for any longer than the duration of the method execution

## 1. Process

4: Developer demonstrates a clear understanding of their own problem solving process. Logically breaks down large problems into manageable challenges. Has a thoughtful, refined strategy for approaching complex challenges. Developer clearly articulates thought processes.

## 2. Fundamental JavaScript & Style

3.5: Application demonstrates excellent knowledge of JavaScript syntax and style, could use some minimal refactoring

## 3. Test-Driven Development & Code Sanitation

4: Application is broken into components which are well tested in both isolation and integration using appropriate data. Linting shows 0 complaints.

## 4. Functional Expectations

4: Application meets all requirements, and implements one extension properly.
