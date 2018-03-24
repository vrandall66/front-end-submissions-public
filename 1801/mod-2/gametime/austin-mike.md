# Game Time
* Students: Mike & Austin
* Evaluator: Leta & Cody

Comments:
* UI: Basic graphics, understandable instructions
* Code: References to DOM in Game.js, functions well separated, using bind in place of an arrow function (it works, but there's a better solution), use of magic numbers
* Test: Want to put action/method/function you're testing in the test name, skipping tests in Game-test.js because it has references to DOM
Workflow: Bunch of commits all at once, few pull requests with lots of commits

### Functional Expectations

Score: 3
Game works, is playable, player doesn't get stuck anywhere.

* 4 - Application is fully playable and exceeds the expectations set by instructors
* 3 - Application is fully playable without crashes or bugs
* 2 - Application has some missing functionality but no crashes
* 1 - Application crashes during normal usage

### User Interface

Score: 3
UI makes sense. Good screens, clear instructions.

* 4 - The application is pleasant, logical, and easy to use. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer.
* 3 - The application has many strong pages/interactions, but a few holes in lesser-used functionality.
* 2 - The application shows effort in the interface, but the result is not effective. The evaluator has some difficulty using the application when reviewing the features in the user stories.
* 1 - The application is confusing or difficult to use.

### Testing

Score: 2-3
Some skipped tests. Testing functions with DOM (move that DOM manipulation into index.js).

* 4 - Project has a running test suite that exercises the application at multiple levels. The test suite covers almost all aspects of the application and uses mocks and stubs when appropriate. ESLint shows 0 complaints.
* 3 - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.
* 2 - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.
* 1 - There is little or no evidence of testing in this application. ESLint shows 10+ complaints.

### JavaScript Style

Score: 3
Similar comments as Application Organization

* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.

### Application Organization

Score: 3
Think about what classes know what, whether or not all parameters are necessary or if the required data is already being passed in via the class constructor

* 3 - Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.

### Workflow

Score: 2-3
Work on making smaller commits and pull requests

* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.
* 2 - The developer/team makes large commits covering multiple features that make it difficult for the evaluator to determine the evolution of the application. The team does not utilize a planning tool or equitable pairing practices. One or both members do not contribute meaningfully to the application.
