# Complete Me
### Student Name: Austin
### Evaluator: Brittany

Comments:
* Make sure you're using a .gitignore file so that you don't commit the node_modules directory to github.
* Articulation needs a lot of work, practice reading docs and highlighting terminology to get yourself more familiar with the proper vocabulary to be using. Pair with as many different upper mod students as possible to get used to the different ways people speak about code.
* You seem to be anticipating that a user will pass in a [word here](https://github.com/Awiedenman/complete-me/blob/master/scripts/Trie.js#L4) but then you're not doing anything with that value.
* A better name for [this variable](https://github.com/Awiedenman/complete-me/blob/master/scripts/Trie.js#L10) would be `lowerCaseLetters`, because you're creating an array of letters and it's no longer a single word any more.
* Missing a [semicolon here](https://github.com/Awiedenman/complete-me/blob/master/scripts/Trie.js#L15)
* Indentation is off [here](https://github.com/Awiedenman/complete-me/blob/master/scripts/Trie.js#L47)
* [This conditional](https://github.com/Awiedenman/complete-me/blob/master/scripts/Trie.js#L44) only moves words that have been selected to the front of the array, and doesn't take into account how many times a word has been selected. e.g. a word selected 5 times should have a weight of 5, and that word should appear before one that has been selected 3 times. Right now you're simply checking if it has been selected or not by checking if the weight is greater than 0.
* I would avoid nesting helper methods like `findWord` in other methods. Break this out into a completely independent method; right now your `suggest` method is really long and difficult to follow.
* [This](https://github.com/Awiedenman/complete-me/blob/master/tests/Trie-test.js#L97) isn't an accurate description of what you're asserting in your test.
* This [test](https://github.com/Awiedenman/complete-me/blob/master/tests/Trie-test.js#L76-L84) isn't making any assertions.
* Make sure not to leave behind debugging statements like [console.logs](https://github.com/Awiedenman/complete-me/blob/master/tests/Trie-test.js#L47) and commented out code.
* In a test like [this](https://github.com/Awiedenman/complete-me/blob/master/tests/Trie-test.js#L63), I would also throw a word in there that *shouldn't* be returned with the rest of the suggestion results. Like 'cat'. And verify that it's not included in the array. Right now you could potentially have a bug in your code that's returning every single word in your trie regardless of the suggestion input.

## 1. Process

2: Developer demonstrates a haphazard, trial and error approach, without clear strategy. Developer does not articulate thought process clearly, and cannot explain the problem-solving strategies they utilized.

## 2. Fundamental JavaScript & Style

2.5: Application runs but the code has long methods, unnecessary or poorly named variables, and needs some refactoring

## 3. Test-Driven Development & Code Sanitation

3: Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. Linting shows five or fewer complaints.

## 4. Functional Expectations

3: Application meets all requirements as laid out per the specification.