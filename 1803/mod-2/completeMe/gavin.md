# Complete Me
### Student Name: Gavin
### Evaluator: Brittany

Comments:
* Articulation and vocabulary is on point, but need a little practice being able to speak about things at a high level (this will just come with repetition) - start simple when someone asks you to describe something at first, and if they need more details they'll dig down with you to get that information. 
* Nice thought process demonstrated throughout the Trie code, thinking of edge cases and keeping methods small, simple and testable.

## 1. Process

3: Developer has strategies for approaching complex challenges. Can explain thought process and strategy when prompted.

## 2. Fundamental JavaScript & Style

3: Application shows strong effort towards organization, content, and refactoring

* [This](https://github.com/gavin-love/tdd/blob/complete-me/lib/Trie.js#L78-L82) is a good use-case for a one-liner:

`dictionary.forEach(word => this.insert(word));`

* Nice job breaking [this](https://github.com/gavin-love/tdd/blob/complete-me/lib/Trie.js#L67) functionality out into a separate method rather than nesting it within your suggest.

* You don't have to name an [array](https://github.com/gavin-love/tdd/blob/complete-me/lib/Trie.js#L51) something with the word 'array' in it. That's kind of like defining something using the word itself. I'd rename this to just `letters`

* Better naming [here](https://github.com/gavin-love/tdd/blob/complete-me/lib/Trie.js#L44-L46) for this method would be something like `getWordCount` -- methods and functions should be verbs because they *do* something, variables should be nouns because they *represent* something. You might also want to look into getters and setters on ES6 classes -- we haven't covered them in class, but it's a new way to have methods that simply return an instance property value.

* You could probably use a forEach [here](https://github.com/gavin-love/tdd/blob/complete-me/lib/Trie.js#L12) instead of a for loop...just a little more readable.

* Nice conditional [check](https://github.com/gavin-love/tdd/blob/complete-me/lib/Trie.js#L21-L24) for avoiding duplicates!


## 3. Test-Driven Development & Code Sanitation

3: Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. Linting shows five or fewer complaints.

## 4. Functional Expectations

3: Application meets all requirements as laid out per the specification.