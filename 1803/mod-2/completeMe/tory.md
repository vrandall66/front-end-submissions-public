# Complete Me
### Student Name: Tory
### Evaluator: Brittany

Comments:
* It's clear you have a problem-solving process in place, and your articulation is accurate concise. Seemed to work through re-implementing suggest through a bit of memorization rather than trying to think about the problem, so I'd like to see a little more pseudo-coding/drawing/writing before you actually jump right into the code.
* Code is clean and readable overall, but definitely has some opportunities for refactoring. Think closely about naming conventions and creating semantic variable/method names. 

## 1. Process


3: Developer has strategies for approaching complex challenges. Can explain thought process and strategy when prompted.


## 2. Fundamental JavaScript & Style

3: Application shows strong effort towards organization, content, and refactoring


* Variable naming could be better [here](https://github.com/tdberg21/complete-me/blob/master/lib/Trie.js#L6-L7). `count` could be more descriptive (wordCount) and you don't have to name an array something with the word 'array' in it. That's kind of like defining something using the word itself. I'd rename this to just `sugesstions`

* The `count` method should be renamed to something like `getCount`. Method and function names should always be verbs, because they *do* something, variables should always be nouns because they represent something

* Not entirely sure what [this](https://github.com/tdberg21/complete-me/blob/master/lib/Trie.js#L18-L20) conditional is doing here. Your trie is automatically starting off with a root node that you set in the constructor, so this should always pass unless you happened to have a delete method that removed the root node.

* Break [this](https://github.com/tdberg21/complete-me/blob/master/lib/Trie.js#L43-L53) function out so that it's something that can be tested -- it contains quite a bit of functionality that you'd want to verify

* Nice job on the contains method!


## 3. Test-Driven Development & Code Sanitation

2.5: Testing suite was a little bare, and there was some functionality in the Trie that's currently unreachable by tests (search functionality within suggest).


## 4. Functional Expectations

4: Application meets all requirements, and implements one extension properly.

* 4 here after implementing `contains`