# Complete Me
### Student Name: LeeLee
### Evaluator: Brittany

Comments:
* Work on slowing down a bit during the problem solving process; seemed like you maybe felt a bit rushed trying to work through the contains method. Take your time and think about the problem before writing any code down. I'd recommend not even pseudocoding in your text editor for a while, pseudocode with pen and paper in order to slow down your thought process a bit.
* JavaScript is sound overall but there are some minor nitpicks and inconsistencies that I'd like you to start cleaning up -- make sure your indentation is accurate, be consistent with your use of semi-colons and braces, etc. Make sure you're enforcing your linter file and correcting any of those errors. This is a really quick, easy win and makes your code look infinitely better and more readable -- this will stand out to potential employers a lot if you take the time to keep your codebase clean and consistent.


## 1. Process


3: Developer has strategies for approaching complex challenges. Can explain thought process and strategy when prompted.

## 2. Fundamental JavaScript & Style

3: Application shows strong effort towards organization, content, and refactoring

* Make sure you use a .gitignore file so that you don't commit files like .DS_Store, node_modules, etc. This will save you a lot of headaches in the future.

* [Value](https://github.com/TwirlingGoddess/Complete-Me/blob/master/lib/Node.js#L3) is kind of a vague name for a property...it's also really common for something to already be using the term 'value', that you might accidentally override. Notice in github how the syntax highlighting is blue for that property and black for the others -- usually that's an indicator that you're using a term you might not want to. I'd rename this to something like 'letter' or 'data'.

* wordCount would be more specific [here](https://github.com/TwirlingGoddess/Complete-Me/blob/master/lib/Trie.js#L6)

* Missing some semicolons [here](https://github.com/TwirlingGoddess/Complete-Me/blob/master/lib/Trie.js#L16-L19)

* You'd want a check [here](https://github.com/TwirlingGoddess/Complete-Me/blob/master/lib/Trie.js#L21-L22) that says 'if this completed word doesn't already exist, set it, and increase the counter. Right now you're increasing the counter no matter what, even if a user tried to insert a duplicate word. I'd put a conditional here that checks to make sure `completedWord` isn't already set to something.

* Break [this](https://github.com/TwirlingGoddess/Complete-Me/blob/master/lib/Trie.js#L34-L44) function out so that it's something that can be tested -- it contains quite a bit of functionality that you'd want to verify

* Nice job on the contains method!

## 3. Test-Driven Development & Code Sanitation

3: Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. Linting shows five or fewer complaints.

## 4. Functional Expectations

4: Application meets all requirements, and implements one extension properly.

* 4 here after implementing `contains`