# Game Time
* Students: David & Quin
* Evaluator: Brittany

Comments:
* Testing is overall really slim, you should probably have about double the amount of assertions that you do. Make sure you're testing every class and every method in each class. If there's something that's untestable, it means you need to do a refactor.
* You'll notice some scores are slightly below 3 -- this isn't something that would prevent you from graduating, I just want you to be aware of where your code truly fell on a spectrum of 1-4

### Functional Expectations

* 4 - Application is fully playable and exceeds the expectations set by instructors

### User Interface

* 3 - The application has many strong pages/interactions, but a few holes in lesser-used functionality.

### Testing

* 2.5 - Project has a running test suite that tests multiple levels but fails to cover some features. Lacking a lot of method tests that would require a refactor

### JavaScript Style

* 2.75 - Application is thoughtfully put together with some duplication and opportunities for refactoring. Developer can speak to choices made in the code.

* Confused about the difference between the gameOver and sessions variables [here](https://github.com/dsdunn/gametime/blob/master/lib/index.js#L37-L38) -- the naming makes it sound like they would represent the same thing.

* This element [selector](https://github.com/dsdunn/gametime/blob/master/lib/index.js#L66) should be in a variable, as you're acccessing it more than once in the file.

* You shouldn't pass in [context](https://github.com/dsdunn/gametime/blob/master/lib/snake.js#L6) as an instance property, but rather just pass it in to the methods that need is as they are invoked. e.g. the only place you need context in this file is in the draw method, so it should be passed in as a parameter to that method instead

### Application Organization

* 3 - Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.

* Filenames for classes should start with a capital letter, just the way class names do.


### Workflow

* 2.75 - The developer/team makes large commits covering multiple features that make it difficult for the evaluator to determine the evolution of the application.

* There is a serious lack of commits here. You have about 25 -- for context, a project of this size should have at least 100 commits, likely a lot more. Work on breaking down smaller pieces of functionality in each commit rather than waiting until an entire feature is done.