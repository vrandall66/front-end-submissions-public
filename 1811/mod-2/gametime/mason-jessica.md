# Game Time
* Students: Mason and Jessica
* Evaluator: Pam

Comments:
* Great UI - really love the recreation of Jeopardy with the different typefaces, the podiums, and color scheme! 
* Form to start play won't accept names longer than 7 characters?
* Bugs: Board disappears completely in Round 2; appears logic is still set to only allow player to guess 4 times before cycling to next round
* Glad to hear that this project was a good learning experience and that you were willing to go back and tackle some of the bugs/issues brought up in the original eval

### Functional Expectations

* [x] Advanced Beginner - Application has some missing functionality but no bugs or broken functionality.

### User Interface

* [x] Proficient - The application has many strong pages/interactions, but a few holes in lesser-used functionality.
* [x] Exceptional -  Meets all expectations for `Proficient`. In addition, the application is pleasant, logical, and easy to use. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer.

### Testing

* [x] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.

* You could move (this)[https://github.com/jessicalyn/jeopardy/blob/master/test/clue-test.js#L28 ] into the `beforeEach` to use for all the tests for `Clue`
* Be careful that you aren't forcing your application to do things it doesn't naturally do in your testing like in line 46 (here)[https://github.com/jessicalyn/jeopardy/blob/master/test/clue-test.js#L46 ]. `playerScore` is called within the `checkAnswer` method that you are checking.
* Make sure every test has all 4 phases - including assertions. 

### JavaScript Style & OOP

* [x] Advanced Beginner - Your application has a significant amount of duplication and one or more major bugs. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. There are one or more major bugs.

* Be sure to name methods by the "action" they are completing - only a few in there, most are named appropriately
* Good job with variable names!
* Game is doing quite a bit of lifting
* Quite a bit of hardcoded values and duplicated code that could be refactored. Opportunities for breaking out methods - `assignCategories` is 143 lines long due to duplicated code

### Workflow

* [x] Proficient - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.