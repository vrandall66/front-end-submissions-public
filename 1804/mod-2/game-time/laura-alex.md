# Game Time
* Students: Laura and Alex
* Evaluator: Brittany Storoz

Comments:
* Both articulated their knowledge of classes/OOP very well
* Little too many things in the index.js that could be moved into the Game class but overall classes seemed well-structured and they each had appropriate methods and instance properties on them

### Functional Expectations

* 3.5 - Application is fully playable without crashes or bugs

* Attempted an extension but didn't quite get there

### User Interface

* 3.5 - The application is pleasant, logical, and easy to use. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer. Couple stylistic things that could improve.

* Able to use the application without any guidance or instruction
* Make a bit more difference in the green of the frog vs. the grass so I can tell I've been killed and have started over
* Prioritize the game by giving it a bit more space, and de-emphasize the instructions/about section by making it more of a sidebar

### Testing

* 4 - Project has a running test suite that exercises the application at multiple levels. The test suite covers almost all aspects of the application and uses mocks and stubs when appropriate. ESLint shows 0 complaints.
* 3 - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.
* 2 - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.
* 1 - There is little or no evidence of testing in this application. ESLint shows 10+ complaints.

### JavaScript Style & OOP

* 4 - Application has exceptionally well-factored code with little or no duplication. SRP (single responsibility principle) and DRY (don’t repeat yourself) principles are utilized. There are zero instances where an instructor would recommend taking a different approach. Application is organized into classes (and correctly uses inheritance) and there are no instances where instructor would suggest moving logic or data to another class. The business-logic code driving functionality is cleanly separated from rendering, view-related code.
* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.
* 2 - Your application has a significant amount of duplication and one or more major bugs. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. There are one or more major bugs.
* 1 - Your client-side application does not function. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Application is not separated into classes, or methods and properties are illogically assigned to classes. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Business-side logic and view-related code is not separated at all.

* Stylistic nitpick, decide whether youre using [single quotes or double quotes](https://github.com/Alexbruce1/game-time/blob/master/lib/Game.js#L19-L20)

### Workflow

* 4 - The developer/team effectively uses Git branches and many small, atomic commits that document the evolution of their application with descriptive commit messages. The team displays good pairing practices (driver-navigator, dividing up work, etc) and utilizes some sort of planning tool (GitHub issues, Waffle, Trello, etc). The team develops a clear MVP (minimum viable product) and conducts a DTR (define the relationship). Both members contribute meaningfully to the application.
* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.
* 2 - The developer/team makes large commits covering multiple features that make it difficult for the evaluator to determine the evolution of the application. The team does not utilize a planning tool or equitable pairing practices. One or both members do not contribute meaningfully to the application.
* 1 - The developer/team committed the code to version control in only a few commits. The evaluator cannot determine the evolution of the application.
* 0 - The application was not checked into version control.

* Nice readable and consistent commit messages