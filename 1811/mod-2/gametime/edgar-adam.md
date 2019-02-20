# Game Time
* Students: Edgar & Adam
* Evaluator: Pam

Comments:

* Nice README!
* Major bug - the game is completely unplayable once a spin happens and a player has an incorrect guess. Errors in the console point to the `highlightActivePlayer` method?

### Functional Expectations

* [x] Novice - Application is unplayable due to lack of functionality or broken logic.

### User Interface

* [x] Proficient - The application has many strong pages/interactions, but a few holes in lesser-used functionality.

### Testing

* [x] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.

* Good effort towards testing. Still some gaps throughout testing suite:

- Be sure that your testing suite isn't forcing behaviors that don't occur in the application like (here)[https://github.com/criteriamor/wheel-of-fortune/blob/master/test/Game-test.js#L91-L109 ]. This is happening in several tests. There is forced reassignment of several values; incorrect arguments passed through
- Remember that you can't test for random results and you should generally be testing for things that are true, not false. (Here)[https://github.com/criteriamor/wheel-of-fortune/blob/master/test/Game-test.js#L50-L55 ] there is always a chance that your method for shuffles things will return the same exact array, making it so this test will fail at random
- Test for all methods on a class (few exceptions) - paying particular attention to any that have conditional logic that result in different outputs/updates (and making sure you are testing for this)


### JavaScript Style & OOP

* [x] Advanced Beginner - Your application has a significant amount of duplication and one or more major bugs. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. There are one or more major bugs.

* Lingering console logs in your `BonusWheel` class. Be sure to keep your codebase tidy
* Opportunities for naming - be sure to name methods by the "action" they are completing. Names make it hard to follow what methods do
* `Game` is doing quite a bit of lifting and has some that would be better handled by the class dealing with that data. A refactor could include making it so that the `Puzzle` class handles all things related to the `Puzzle`.

### Workflow

* [x] Proficient - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.