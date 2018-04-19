# Complete Me
### Evaluator: Jhun

### Comments:
* line 27 of `Trie` is cool. Maybe consider using the spread operator next time.
* line 33/46 of `Trie` I don't think you need to return anything. You're asking if something isn't there and returning nothing. You could just return out of the function.
* getSuggestions is pushing to an array inside the object, but when you call the `suggest` function initially you reset the suggestions array. Would it make sense to just sort and set what's sorted as the `sortedSuggestions` prop?
* Thanks for breaking some functions into small pieces.

### 1. Process

* 4: Developer demonstrates a clear understanding of their own problem solving process. Logically breaks down large problems into manageable challenges. Has a thoughtful, refined strategy for approaching complex challenges. Developer clearly articulates thought processes.

### 2. Fundamental JavaScript & Style

* 3:  Application shows strong effort towards organization, content, and refactoring

### 3. Test-Driven Development & Code Sanitation

* 3.5: Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. Linting shows five or fewer complaints.

### 4. Functional Expectations

* 4: Application meets all requirements, and implements one extension properly.
