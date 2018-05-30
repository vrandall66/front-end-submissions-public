# Complete Me
### Student Name: Kevin
### Evaluator: Brittany

Comments:
*
*
*

## 1. Process

4: Developer demonstrates a clear understanding of their own problem solving process. Logically breaks down large problems into manageable challenges. Has a thoughtful, refined strategy for approaching complex challenges. Developer clearly articulates thought processes.
3: Developer has strategies for approaching complex challenges. Can explain thought process and strategy when prompted.
2: Developer demonstrates a haphazard, trial and error approach, without clear strategy. Developer does not articulate thought process clearly, and cannot explain the problem-solving strategies they utilized.
1: Developer does not demonstrate any strategy or process. No meaningful code is written and developer cannot articulate their process.

## 2. Fundamental JavaScript & Style

3: Application shows strong effort towards organization, content, and refactoring

* Make sure you use a .gitignore file so that you don't commit files like .DS_Store, node_modules, etc. This will save you a lot of headaches in the future.

* `wordCount` would be a better name [here](https://github.com/kevinkrom787/complete-me/blob/master/lib/Tree.js#L7), counter is a little vague and also might sound more like a method than a variable

* Ahhh, naming a variable [array](https://github.com/kevinkrom787/complete-me/blob/master/lib/Tree.js#L12) is really uninformative. What's in the array? Letters? What does it represent?

* Using a while loop [here](https://github.com/kevinkrom787/complete-me/blob/master/lib/Tree.js#L14) on array.length isn't the most intuitive...I would have to know that you're popping or shifting things out of the array in order for that length be changing, otherwise it just seems like this while loop is going to run forever.

* Not sure you really need to be calling [count](https://github.com/kevinkrom787/complete-me/blob/master/lib/Tree.js#L26) here


## 3. Test-Driven Development & Code Sanitation

4: Application is broken into components which are well tested in both isolation and integration using appropriate data. Linting shows 0 complaints.
3: Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. Linting shows five or fewer complaints.
2: Application makes some use of tests, but the coverage is insufficient. Linting shows ten or fewer complaints.
1: Application does not demonstrate strong use of TDD. Linting shows more than ten complaints.

## 4. Functional Expectations

4: Application meets all requirements, and implements one extension properly.

* 4 here for annotating your code and implementing select