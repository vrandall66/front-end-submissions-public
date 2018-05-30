# Complete Me
### Student Name: Kevin
### Evaluator: Brittany

Comments:
* JS does not always clearly demonstrate a logical thought process, and there is difficult thinking through problems on the fly
* Needs more practice whiteboarding/pseudocoding/thinking things through before trying to code them out
* Articulation and explanation of what's happening in code seems a bit flustered and unsure, more confidence and understanding of fundamental patterns and concepts would help

## 1. Process

2.5: Developer demonstrates a haphazard, trial and error approach, without clear strategy. Developer can come close to a solution, but struggles to do it eloquently and has a difficult time responding to prompting/redirection.


## 2. Fundamental JavaScript & Style

2.5: Application shows strong effort towards organization, content, and refactoring but also some gaps in the problem-solving process and demonstrated several places for refactoring.

* Make sure you use a .gitignore file so that you don't commit files like .DS_Store, node_modules, etc. This will save you a lot of headaches in the future.

* `wordCount` would be a better name [here](https://github.com/kevinkrom787/complete-me/blob/master/lib/Tree.js#L7), counter is a little vague and also might sound more like a method than a variable

* Ahhh, naming a variable [array](https://github.com/kevinkrom787/complete-me/blob/master/lib/Tree.js#L12) is really uninformative. What's in the array? Letters? What does it represent? [ArrayOne](https://github.com/kevinkrom787/complete-me/blob/master/lib/Tree.js#L89) is even worse.

* Using a while loop [here](https://github.com/kevinkrom787/complete-me/blob/master/lib/Tree.js#L14) on array.length isn't the most intuitive...I would have to know that you're popping or shifting things out of the array in order for that length be changing, otherwise it just seems like this while loop is going to run forever.

* Not sure you really need to be calling [count](https://github.com/kevinkrom787/complete-me/blob/master/lib/Tree.js#L26) here

* [This](https://github.com/kevinkrom787/complete-me/blob/master/lib/Tree.js#L33-L37) is a good use-case for a one-liner:

`dictionary.forEach(word => this.insert(word));`

* Don't commit console logs. There's a lot in your `select` method -- make sure those are removed before you commit to master.


## 3. Test-Driven Development & Code Sanitation

3: Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. Linting shows five or fewer complaints.
## 4. Functional Expectations

4: Application meets all requirements, and implements one extension properly.

* 4 here for annotating your code and implementing select but your annotations are still a bit off:

* // need an array to push nodes/characters into -- what are you actually pushing into the array? is it nodes? is it characters? what is a character? be explicit -- otherwise I'd assume you don't know what the array actually includes.
*   // base case = when currentNode.children === []; - that doesn't actually represent a base case at all. It's not doing anything. It's simply setting a variable. There's no exit of any form in this line.