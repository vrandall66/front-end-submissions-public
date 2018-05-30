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

* [Value](https://github.com/gavin-love/tdd/blob/complete-me/lib/Node.js#L3) is kind of a vague name for a property...it's also really common for something to already be using the term 'value', that you might accidentally override. Notice in github how the syntax highlighting is blue for that property and black for the others -- usually that's an indicator that you're using a term you might not want to. I'd rename this to something like 'letter' or 'data'.

* Nodes shouldn't need a [suggestions](https://github.com/gavin-love/tdd/blob/complete-me/lib/Node.js#L5) array. It looks like you're not using this so maybe you're aware, but make sure any dead or old code gets taken out before pushing to master.

* If you're going to be working with an instance property of [suggestions](https://github.com/gavin-love/tdd/blob/complete-me/lib/Trie.js#L49) in one of your methods, you should set it equal to an empty array up top in your constructor too. It's just a nice clear way to indicate what types of information the class is going to keep track of. That said, this doesn't necessarily need to be an instance property. You could just make this a variable called `suggestions` within your method, and not set it as an instance property on the class. Because that data changes and resets every time the suggest method is called, and *only* when the suggest method is called, it's data that's pretty specific to and encapsulated within that method.

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