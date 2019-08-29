# FitLit
* Students: Kayla & Amanda
* Evaluator: Brittany

## Rubric

### Functional Expectations
* [ ] 4: Application fulfills all expectations of iterations 1 - 5 with no bugs or missing functionality *as well as* [ ] an extension.
* [x] 3: Application fulfills expectations of iterations 1 - 5 with no bugs or missing functionality.
* [ ] 2: Application is usable but has some missing functionality.
* [ ] 1: Application crashes during normal usage.


### Fundamental JavaScript & Style
* [ ] 4: Application demonstrates excellent knowledge of JavaScript syntax, style, and refactoring.
* [ ] 3: Class methods use array and object prototypes - `for` loops are not used in the application. Application shows strong effort towards organization, content, and refactoring. 
* [ ] 2: Class methods use a mix of array and object prototypes and `for` loops. Application runs but the code has long methods, unnecessary or poorly named variables, and needs significant refactoring.
* [ ] 1: Application generates syntax error or crashes during execution.

### Test-Driven Development
* [ ] 4: Application is broken into components which are well tested in both isolation and integration using appropriate data. Test feature many sad paths for methods as well.
* [ ] 3: All classes and methods are tested. Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. Tests use smaller, sample data files as input rather than the large, original data files.
* [ ] 2: Application makes some use of tests, but the coverage is insufficient given project requirements.
* [ ] 1: Application does not demonstrate strong use of TDD.

* I'd put your mock data [in a directory called mocks under your test directory](https://github.com/Asilo5/fitlit-starter-kit/blob/master/test/Activity-test.js#L4-L5) rather than in your actual data directory. This makes it clearer that certain data is for testing purposes only, not being used as actual application data.


* `avgNumOfKey` is probably not the best name for a [method here](https://github.com/Asilo5/fitlit-starter-kit/blob/master/test/Activity-test.js#L43-L46) -- but that's besides the point. Break these expectations out into separate it blocks. I would say any time you are giving different input to a method, and expecting different output based on that input, that warrants its own it block.



### Encapsulation / Breaking Logic into Components
* [ ] 4: Application is expertly divided into logical components each with a clear, single responsibility.
* [ ] 3: Application effectively breaks logical components apart but breaks the principle of SRP.
* [ ] 2: Application shows some effort to break logic into components, but the divisions are inconsistent or unclear.
* [ ] 1: Application logic shows poor decomposition with too much logic mashed together.


### User Interface
* [x] 4: The application is pleasant, logical, and easy to understand. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer.
* [ ] 3: The application has many strong displays/interactions, but a few holes in lesser-used displays.
* [ ] 2: The application shows effort in the interface, but the result is not effective. The evaluator has some difficulty using the application when reviewing the features in the users' needs.
* [ ] 1: The application is confusing or difficult to use.

* Alignment in places like [this](https://imgur.com/zSgQS4s) is a little off on my machine. It may have lined up great on another monitor, but be sure to test these things out on multiple machines/TVs just to check if it might get a little skewed.

* I love the css transition/tabs that expand and collapse for each dataset, but put hover states on them so that I know they are clickable!

* I'd like to see another font used to differentiate heading text vs. body text. It's a little hard to denote the heirarchy of the content when everything is in the same font! I like the one you've chosen for your headings -- but for any of the actual data numbers, I'd put these in a slightly smaller/more boring font so that the headings can really pop.

* OVerall very nice and clean and not overwhelming, I love how simple you kept it showing just a single data section at a time rather than putting it all on the page all at once!


### Workflow
* [ ] 4: The team effectively uses Git branches and many small, atomic commits that document the evolution of their application with descriptive commit messages. The team displays good pairing practices (driver-navigator, dividing up work, etc.) and utilizes a planning tool more than GitHub issues (GitHub Projects, Trello, etc).
* [x] 3: The team makes a series of small, atomic commits that document the evolution of their application. The team conducts a DTR (define the relationship) and utilizes GitHub issues and best pairing practices. Both members contribute meaningfully to the application.
* [ ] 2: The team makes large commits covering multiple features that make it difficult for the evaluator to determine the evolution of the application. The team does not utilize a planning tool or equitable pairing practices. One or both members do not contribute meaningfully to the application.
* [ ] 1: The team committed the code to version control in only a few commits. The evaluator cannot determine the evolution of the application.

* README could use a bit of formatting fixups (e.g. npm install command is not written in that code format), your author names are on separate lines that looks a little weird, etc. In the instructions I'd also tell the person to open up the `src/index.html` file in their browser to see the working app

* Very nice consistent commit messages that make it easy to read through the history -- but definitely not enough commits! This is a sign that you're doing way too much work in a single commit and you want to break it into multiple commits. Finding this stopping point for when to commit can be hard and takes practice, but know that you both want to be committing less code more frequently and you'll start to get the feel for it. For reference, you'd probably want at least 3 times as many commits as you both currently have. Probably even quadrouple :)

* Looks like a good even division of labor and switching of driver/navigator