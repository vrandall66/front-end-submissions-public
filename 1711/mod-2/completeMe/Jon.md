## Complete Me Scores
### Student: Jon

### Evaluator:
Brittany

### Evaluator comments: Code style is a little cumbersome and difficult to follow at times, you're doing a lot more work in places where simpler solutions would suffice.


### 1. Fundamental JavaScript & Style

* 3:  Application shows strong effort towards organization, content, and refactoring

* Glad to see you went back and refactored your trie to have that root node

* As mentioned in the eval, there's probably no real reason to break [this](https://github.com/JSweet314/prefix-trie/blob/master/lib/Trie.js#L31-L36) out into another method. You're essentially just pushing the user straight into another method for no real reason.

* I get what you're doing [here](https://github.com/JSweet314/prefix-trie/blob/master/lib/Trie.js#L22), but the if condition is really difficult to follow for someone new reading this code. Checking if `word.length === 1` doesn't tell me anything semantic about what's happening at the moment. I'd rather see this broken out into a variable with a name that means something about what condition has actually been met in plain English. Same thing [here](https://github.com/JSweet314/prefix-trie/blob/master/lib/Trie.js#L49) -- I think making semantic variable names for this type of logic would go a long way with making your code easier to follow.

* Also as mentioned in the eval, a while loop would be a bit more readable and maintainable in the insert method rather than doing this recursively. 


### 2. Test-Driven Development

* 4: Application is broken into components which are well tested in both isolation and integration using appropriate data

### 3. Encapsulation / Breaking Logic into Components

* 4: Application is expertly divided into logical components each with a clear, single responsibility

### 4. Functional Expectations

* 3: Application meets all requirements as laid out per the specification.
