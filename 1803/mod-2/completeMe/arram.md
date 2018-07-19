# Complete Me
### Student Name: Arram
### Evaluator: Brittany

Comments:
* Really nice problem-solving process, super methodical and responded really well to prompting/questions rather than freezing up
* JavaScript is clean and readable, demonstrates a logical thought process. Simple solutions where nothing is overengineered.

## 1. Process

4: Developer demonstrates a clear understanding of their own problem solving process. Logically breaks down large problems into manageable challenges. Has a thoughtful, refined strategy for approaching complex challenges. Developer clearly articulates thought processes.

## 2. Fundamental JavaScript & Style

3: Application shows strong effort towards organization, content, and refactoring

* There should be some sort of flag on your Node class that says if a particular node marks the end of a word -- something like `completedWord` which could either represent a boolean value or a string of the word that node finishes. Looks like you're doing that [here](https://github.com/airum82/complete-me/blob/master/lib/Trie.js#L19-L22) but your Node class doesn't reflect that.

* wordCount would be a bit more specific than just [count](https://github.com/airum82/complete-me/blob/master/lib/Trie.js#L6)

* Don't name arrays with the word [array](https://github.com/airum82/complete-me/blob/master/lib/Trie.js#L10) in them -- that's kind of like defining a term using the term itself. I'd just name this `letters`. Likewise, [entryArray](https://github.com/airum82/complete-me/blob/master/lib/Trie.js#L30) could be renamed to something like `searchPrefix` or `prefixLetters`

* Break [this](https://github.com/airum82/complete-me/blob/master/lib/Trie.js#L36-L44) function out so that it's something that can be tested -- it contains quite a bit of functionality that you'd want to verify

* The `counter` method should be renamed to something like `getCount`. Method and function names should always be verbs, because they *do* something, variables should always be nouns because they represent something. You might also want to look into getters and setters on ES6 classes -- we haven't covered them in class, but it's a new way to have methods that simply return an instance property value.

## 3. Test-Driven Development & Code Sanitation

3: Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. Linting shows five or fewer complaints.

## 4. Functional Expectations

3: Application meets all requirements as laid out per the specification.