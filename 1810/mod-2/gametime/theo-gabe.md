# Game Time
* Students: Theo and Gabe
* Evaluator: Robbie

Comments:
* Careful with the fading colors overlapping with clue colors
* Wager title needed - some styling for input labels needed, text is small compared to input text
* Some bug in the final total/winner calculation
* Can be more detailed about the assertions being made in some tests (beyond array length, test what should be contained in the array)
* Careful with variable names with data types

### Functional Expectations

* 3 - Application is fully playable without crashes or bugs

### User Interface

* 4 - The application is pleasant, logical, and easy to use. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer.

### Testing

* 2 - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.

- Testing is lacking assertions and a little messy because of the local/global object conflicts

### JavaScript Style & OOP

* 2 - Your application has a significant amount of duplication and one or more major bugs. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. There are one or more major bugs.

**Now 3**

- Have many global objects other than game (round, round3, clue) - need to at least get `round3` out of the global scope.

This has been fixed so that only the `game` class is global. Tests have been changed to reflect these changes as well.

### Workflow

* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.

- Some PR merging issues (may be around stashing); replicate your workflow to see if you can reproduce the error to make sure it doesn't happen in groups again.