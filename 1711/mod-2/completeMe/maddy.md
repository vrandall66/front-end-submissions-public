## Complete Me Scores
### Student: Maddy

### Evaluator: Brittany

### Evaluator comments: Very nice thorough testing of edge-cases, impressive that you had the foresight for catching most of those sad-path test cases. 


### 1. Fundamental JavaScript & Style

* 4:  Application demonstrates excellent knowledge of JavaScript syntax, style, and refactoring

* Don't love [this](https://github.com/mmdberg/Complete-Me/blob/master/lib/Trie.js#L38) if condition. I'd rather you break out that find logic into a separate line and save it as a variable so that you can just do an if on that variable value rather than evaluating that line of code in place.

* Overall very nice, clean and readable code. Methods are concise and easy to follow along with.

* [These lines](https://github.com/mmdberg/Complete-Me/blob/master/lib/Trie.js#L30-L31) are used pretty frequently in all of your methods, which means they *could* be refactored out into something else to DRY up your code, but I think in this case it's the right call to leave that duplication in place.

### 2. Test-Driven Development

* 4: Application is broken into components which are well tested in both isolation and integration using appropriate data

### 3. Encapsulation / Breaking Logic into Components

* 4: Application is expertly divided into logical components each with a clear, single responsibility

### 4. Functional Expectations

* 3: Application meets all requirements as laid out per the specification.

