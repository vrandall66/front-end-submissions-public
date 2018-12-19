# Game Time
* Students: Elly & David
* Evaluator: Pam

Comments:

* The UI looks _really_ good. Lots of nice touches with UX
* Major Bugs: 
1. Answer to puzzle shows when highlighting board with mouse - important one that should really be fixed and not just added as an issue
2. Application allows for selecting an infinite amount of letters on the board without spinning _OR_ after a player has completed a spin. Logic is missing to properly end the player's turn.
* Remove commented out code

**Given extension to DM link to updated repo with fixes (complete testing and fix bug mentioned above) before 12/14 at 10:00AM.**

### Functional Expectations

* 2 - Application has some missing functionality but no crashes

### User Interface

* 4 - The application is pleasant, logical, and easy to use. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer.

### Testing

* 1 - There is little or no evidence of testing in this application.

**AFTER RESUBMISSION***

- Make sure that you you're testing the actual output of the methods on the class. There were a number of tests that were testing methods on a class that had no assertions that checked actual functionality.
- If there is conditional logic within a method being tested, make sure that you check that the conditional logic is working
- Make sure you are only passing arguments in your test when your methods are set up for those parameters 

* 2 - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.

### JavaScript Style & OOP

* 2 - Your application has a significant amount of duplication and one or more major bugs. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. There are one or more major bugs.

### Workflow

* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.
