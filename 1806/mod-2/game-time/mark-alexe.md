# Game Time
* Students: Mark & Alex E
* Evaluator: Brittany

Comments:
* Cute snake :) Though it needs its own class
* Some refactoring opportunities for methods and properties for particular objects, but decent demonstration that OOP skills are in place

### Functional Expectations

* 3 - Application is fully playable without crashes or bugs

### User Interface

* 3 - The application has many strong pages/interactions, but a few holes in lesser-used functionality.

### Testing

* 3 - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.

* Solid refactoring to include the Snake class & test it over the weekend but with tests like [this](https://github.com/alexanderela/game-time/blob/master/test/snake-test.js#L55-L59) make sure you are asserting a particular length first, then calling `growSnake`, then asserting the new length. Tough for me to tell by this test alone if the snake always has a length of 9 or if it's actually growing. What's it's original length?

### JavaScript Style & OOP

* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.


### Workflow

* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.

* Really nice commit messages - consistent and readable. A+!

* Try to never commit commented out code, like [here](https://github.com/alexanderela/game-time/commit/02ca49aad42c06ae1117475dac551c3cdf14538e). If you were to pull request this, it would make it really hard for the other developer to read the diff and understand exactly what's happening.

