# Game Time
* Students: Isaac & Tom
* Evaluator: Pam

Comments:
* Overall, UI colors look good! The text is very small - and I'm unable to see the entire GameBoard on my screen - making it difficult to use the game itself.  
* Update UX so that wheel spins to color and there is some visual indication of the wheel element that has been chosen
* Although not a requirement for this project, I would encourage you to update your README per the recommendations we went over in the Github Collab lesson
* Several bugs that were not presented/revealed/found in evaluation: Can buy a vowel with no money; wheel spins before the next player's turn starts; wheel values change _every_ turn so that a new values are being used throughout the round (not per spec); UX does not clearly show how to guess an answer; bug showing duplicated letters still present (in Bonus Round)

*Given extension until 2/8 at 5PM to make bugs/areas lacking from remote eval. Resubmitted changes within an hour that adjusted test but did not fix broken functionality around duplicated letters showing on gameboard*

### Functional Expectations

* [x] Advanced Beginner - Application has some missing functionality but no bugs or broken functionality. (Several bugs and broken functionality)

### User Interface

* [x] Advanced Beginner - The application shows effort in the interface, but the result is not effective. The evaluator has some difficulty using the application when reviewing the features in the user stories.

### Testing

* [x] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.

* (These tests [https://github.com/IsaacSunoo/WheelOfFortune/blob/master/test/wheel-test.js#L24-L30]) need fleshed out
* Opportunities for improving testing before each method is called (checking values before running methods)[https://github.com/IsaacSunoo/WheelOfFortune/blob/master/test/wheel-test.js#L24-L30 ]
* Testing in `Game` could be improved - make sure that you are testing your conditionals as well as side effects that methods are causing.

### JavaScript Style & OOP

* [x] Advanced Beginner - Your application has a significant amount of duplication and one or more major bugs. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. There are one or more major bugs.

* Good job articulating what is happening in certain methods
* `Game` class is doing lots of heavy lifting. There are quite a few longer methods that could be refactored.
* Major bugs in the codebase (see summary at top of rubric).

### Workflow

* [x] Proficient - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.