# Game Time
* Students: Michael King-Stockton and Michael Krog
* Evaluator: Robbie


### Functional Expectations

* [ ] Novice - Application is unplayable due to lack of functionality or broken logic.
* [ ] Advanced Beginner - Application has some missing functionality but no bugs or broken functionality.
* [X] Proficient - Application is fully playable and meets all requirements of the spec.
* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, the application exceeds the expectations set by instructors.


### User Interface

* [ ] Novice - The application is confusing or difficult to use.
* [ ] Advanced Beginner - The application shows effort in the interface, but the result is not effective. The evaluator has some difficulty using the application when reviewing the features in the user stories.
* [X] Proficient - The application has many strong pages/interactions, but a few holes in lesser-used functionality.
* [ ] Exceptional -  Meets all expectations for `Proficient`. In addition, the application is pleasant, logical, and easy to use. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer.

* The animations are a nice touch. They change a little too frequently for me - a bit distracting while playing the game. Can keep them but tone them down a bit.
* I like the opening screen - the player inputs look super slick
* The UI feedback when an answer is given is nice

### Testing

* [ ] Novice - There is little or no evidence of testing in this application. ESLint shows 10+ complaints.
* [X] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.
* [ ] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.
* [ ] Exceptional - Meets all requires of `Proficient`. In addition, the test suite makes use of mocks and stubs when appropriate. ESLint shows 0 complaints.

* At first glance there are a lot of tests! Although many of them are centered around instantiation of the classes and some tests are for behavior/methods of the classes. Would like to see more emphasis on method testing in the future. There are a lot of untested methods.
* Nice job using the `beforeEach()` hook to DRY up tests


### JavaScript Style & OOP

* [ ] Novice - Your client-side application does not function. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Application is not separated into classes, or methods and properties are illogically assigned to classes. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Business-side logic and view-related code is not separated.
* [ ] Advanced Beginner - Your application has a significant amount of duplication and one or more major bugs. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. There are one or more major bugs.
* [X] Proficient - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.
* [ ] Exceptional - Meets all requirements of `Proficient`. In addition, application has exceptionally well-factored code with little or no duplication. SRP (single responsibility principle) and DRY (don't repeat yourself) principles are utilized. There are _zero_ instances where an instructor would recommend taking a different approach. Application is organized into classes (and correctly uses inheritance) and there are no instances where instructor would suggest moving logic or data to another class. The business-logic code driving functionality is cleanly separated from rendering, view-related code.

* Do not name variables using data types, and be more specific as in [this case](https://github.com/MRKrog/Jeopardy_GameTime/blob/master/src/Round.js#L34). If you looked at this now, you wouldn't know what `reducedArr` is.
* Good job extracting DOM manipulation functions to the domUpdates file
* Some methods are getting quite long, like [this one](https://github.com/MRKrog/Jeopardy_GameTime/blob/master/src/dailyDouble.js#L9-L27). When methods start to exceed 10 lines, look for refactoring opportunities.

### Workflow
* [ ] Novice - The developer/team committed the code to version control in only a few commits. The evaluator cannot determine the evolution of the application.
* [ ] Advanced Beginner - The developer/team makes large commits covering multiple features that make it difficult for the evaluator to determine the evolution of the application. The team does not utilize a planning tool or equitable pairing practices. One or both members do not contribute meaningfully to the application.
* [X] Proficient - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.
* [ ] Exceptional - Meets all requirements for `Proficient`. In addition, the developer/team effectively uses Git branches and many small, atomic commits that document the evolution of their application with descriptive commit messages. The team displays good pairing practices (driver-navigator, dividing up work, etc) and utilizes some sort of planning tool (GitHub issues, Waffle, Trello, etc). The team develops a clear MVP (minimum viable product) and conducts a DTR (define the relationship). Both members contribute meaningfully to the application.

* Careful with committing `.DS_Store` files. These are extra files created by Macs when you use Finder. Add this file to your `.gitignore` for future projects.