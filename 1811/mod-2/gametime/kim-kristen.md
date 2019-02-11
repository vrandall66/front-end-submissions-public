# Game Time
* Students: Kim & Kristen
* Evaluator: Brittany

Comments:
* Really nice effort going back to fix feedback and polish up the UI
* Good demonstration by both partners of dividing work evenly and contributing to each part of the codebase
* Sound OOP structure and tests to accompany it -- despite lack of time it seems like all areas of the rubric had solid effort put into them and nothing fell to the wayside. Well-rounded.

### Functional Expectations

* [ ] Novice - Application is unplayable due to lack of functionality or broken logic.
* [ ] Advanced Beginner - Application has some missing functionality but no bugs or broken functionality.
* [x] Proficient - Application is fully playable and meets all requirements of the spec.
* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, the application exceeds the expectations set by instructors.


### User Interface

* [ ] Novice - The application is confusing or difficult to use.
* [ ] Advanced Beginner - The application shows effort in the interface, but the result is not effective. The evaluator has some difficulty using the application when reviewing the features in the user stories.
* [x] Proficient - The application has many strong pages/interactions, but a few holes in lesser-used functionality.
* [ ] Exceptional -  Meets all expectations for `Proficient`. In addition, the application is pleasant, logical, and easy to use. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer.

* Nice splash screen and effort at only showing the context that you need at any given time.

* Good job going back to emphasize active/disabled states and hover states on your elemets

### Testing

* [ ] Novice - There is little or no evidence of testing in this application. ESLint shows 10+ complaints.
* [ ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.
* [x] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.
* [ ] Exceptional - Meets all requires of `Proficient`. In addition, the test suite makes use of mocks and stubs when appropriate. ESLint shows 0 complaints.


* [This](https://github.com/kimmichurri/coin-star/blob/master/test/game-test.js#L66) test is probably asserting a bit too much and could be broken out into multiple it blocks. Usually whenever you have the word 'and' in your it block description, it means it's gunna try to test too much at once. I'd break this out into two separate it blocks - one for asserting against the puzzles and another for asserting against the player coins. I'd also make sure the round coins got reset to zero when the round incremented.

* Descriptions could use a little work e.g. [this](https://github.com/kimmichurri/coin-star/blob/master/test/game-test.js#L94) one might be re-written as 'it should instantiate a new bonus wheel when bonusRound is called'


### JavaScript Style & OOP

* [ ] Novice - Your client-side application does not function. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Application is not separated into classes, or methods and properties are illogically assigned to classes. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Business-side logic and view-related code is not separated.
* [ ] Advanced Beginner - Your application has a significant amount of duplication and one or more major bugs. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. There are one or more major bugs.
* [x] Proficient - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.
* [ ] Exceptional - Meets all requirements of `Proficient`. In addition, application has exceptionally well-factored code with little or no duplication. SRP (single responsibility principle) and DRY (don't repeat yourself) principles are utilized. There are _zero_ instances where an instructor would recommend taking a different approach. Application is organized into classes (and correctly uses inheritance) and there are no instances where instructor would suggest moving logic or data to another class. The business-logic code driving functionality is cleanly separated from rendering, view-related code.

* Overall solid understanding of where instance properties and behaviors should live amongst your classes, slight room for improvement when it comes to refactoring (e.g. we can make [this](https://github.com/kimmichurri/coin-star/blob/master/src/scripts/Game.js#L31-L38) a little more dynamic with a loop and a template literal) but no major concerns

* Some areas where naming conventions are a bit off e.g. [bonusRound](https://github.com/kimmichurri/coin-star/blob/master/src/scripts/Game.js#L91) is a method that performs an action, so it should be named as a verb like 'startBonusRound' or something rather than named as a noun.


### Workflow
* [ ] Novice - The developer/team committed the code to version control in only a few commits. The evaluator cannot determine the evolution of the application.
* [ ] Advanced Beginner - The developer/team makes large commits covering multiple features that make it difficult for the evaluator to determine the evolution of the application. The team does not utilize a planning tool or equitable pairing practices. One or both members do not contribute meaningfully to the application.
* [ ] Proficient - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.
* [x] Exceptional - Meets all requirements for `Proficient`. In addition, the developer/team effectively uses Git branches and many small, atomic commits that document the evolution of their application with descriptive commit messages. The team displays good pairing practices (driver-navigator, dividing up work, etc) and utilizes some sort of planning tool (GitHub issues, Waffle, Trello, etc). The team develops a clear MVP (minimum viable product) and conducts a DTR (define the relationship). Both members contribute meaningfully to the application.

* Nice division of labor and really nice, readable commit messages that are consistent and easy to follow. (Though usually we want them to all start with a capital letter)