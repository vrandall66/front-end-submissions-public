# Complete Me
### Student Name: Tim
### Evaluator: Brittany

Comments:
* Really good with responding to prompting/guidance during the problem-solving process. Though a little unsure where to start, did well coding out a final solution after talking through it with paper and pencil. Yay!
* What is this [comma file](https://github.com/TFisch/complete_me/blob/master/%2C)?

## 1. Process

3: Developer has strategies for approaching complex challenges. Can explain thought process and strategy when prompted.

## 2. Fundamental JavaScript & Style

3: Application shows strong effort towards organization, content, and refactoring

* Rather than having `endOfWord` represent a [boolean](https://github.com/TFisch/complete_me/blob/master/lib/Node.js#L3), you could default it to null then replace it with the completed word value. This makes some other trie logic a bit easier (e.g. finding a particular word, you could traverse down to the last letter and simply return the value of `endOfWord` back rather than checking if `endOfWord` is true, then returning what the user searched for)
* Creating a function inside of a method like [this](https://github.com/TFisch/complete_me/blob/master/lib/PrefixTrie.js#L47-L57) makes your code harder to test. Break this out into it's own method.
* I think I'd prefer if your Node class had some sort of `data` or `value` property to hold the letter that it represents. I see you're using the letters as keys under children which also works well, but having a designated property for that value might be a bit more explicit/readable.

## 3. Test-Driven Development & Code Sanitation

4: Application is broken into components which are well tested in both isolation and integration using appropriate data. Linting shows 0 complaints.
3: Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. Linting shows five or fewer complaints.
2: Application makes some use of tests, but the coverage is insufficient. Linting shows ten or fewer complaints.
1: Application does not demonstrate strong use of TDD. Linting shows more than ten complaints.

* Some of [these](https://github.com/TFisch/complete_me/blob/master/test/PrefixTrie-test.js#L15-L33) are a little redundant. I would simply assert that count is defaulted to 0 (maybe in a separate it block that asserts against default instance properties), then assert that it updates based on how many words are inserted.

* Insert should also test that no new nodes are added if you try to add a duplicate word.

* [This](https://github.com/TFisch/complete_me/blob/master/test/PrefixTrie-test.js#L55-L57) it block doesn't have any assertions in it.

* In [this](https://github.com/TFisch/complete_me/blob/master/test/PrefixTrie-test.js#L72-L78) test I would also insert a word that *doesn't* start with the letter c, and make sure it doesn't make it into the suggestions array. As the test is written now, it could potentially just be returning an array of all the words in the trie.


## 4. Functional Expectations

4: Application meets all requirements, and implements one extension properly.

* Delete completed upon eval