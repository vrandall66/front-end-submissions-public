## Complete Me Scores
### Student: Aldo

### Evaluator:
Brittany

### Evaluator comments: Great job with testing your edge-cases and potential failures, nice easy to read logic and consistent stylistic decisions.


### 1. Fundamental JavaScript & Style

* 4:  Application demonstrates excellent knowledge of JavaScript syntax, style, and refactoring

* Instead of trying to do an implicit return [here](https://github.com/amercado1014/complete-me/blob/master/lib/Trie.js#L34-L35) I'd just break this out into separate lines wrapped in curly braces. Looks like you were avoiding the 80-character line limit. In cases like that, just do the standard:

```
Object.keys(currentNode).find(letter => {
  return letter === currentLetter;
});
```

* Rather than constantly referencing nodeObjectLetter [here](https://github.com/amercado1014/complete-me/blob/master/lib/Trie.js#L53-L64), I'd store that in a variable. It's a little hard to read as-is and you're using it in quite a few places.

* Implicit return would work nicely [here](https://github.com/amercado1014/complete-me/blob/master/lib/Trie.js#L73-L75) with this simple bit of logic ;)


### 2. Test-Driven Development

* 4: Application is broken into components which are well tested in both isolation and integration using appropriate data

### 3. Encapsulation / Breaking Logic into Components

* 4: Application is expertly divided into logical components each with a clear, single responsibility


### 4. Functional Expectations

* 3: Application meets all requirements as laid out per the specification.
