# Game Time
* Students: Sally & Duy
* Evaluator: Brittany

Comments:
* Overall decent organization of code and demonstrated understanding of where certain instance properties/behaviors should live
* Naming conventions need a bit of work to improve readability for other developers
* UI could benefit from having some clearer active/disabled states and hover/clickable states on certain elements. I want to know what's important when, and de-emphasize everything else

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

### Testing

* [ ] Novice - There is little or no evidence of testing in this application. ESLint shows 10+ complaints.
* [ ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.
* [x] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.
* [ ] Exceptional - Meets all requires of `Proficient`. In addition, the test suite makes use of mocks and stubs when appropriate. ESLint shows 0 complaints.


* [Thumbs up](https://github.com/Rosebud303/Jeopardy/blob/master/test/player-test.js#L28-L44)

### JavaScript Style & OOP

* [ ] Novice - Your client-side application does not function. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Application is not separated into classes, or methods and properties are illogically assigned to classes. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Business-side logic and view-related code is not separated.
* [x] Advanced Beginner - Your application has a significant amount of duplication and one or more major bugs. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. There are one or more major bugs.
* [ ] Proficient - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.
* [ ] Exceptional - Meets all requirements of `Proficient`. In addition, application has exceptionally well-factored code with little or no duplication. SRP (single responsibility principle) and DRY (don't repeat yourself) principles are utilized. There are _zero_ instances where an instructor would recommend taking a different approach. Application is organized into classes (and correctly uses inheritance) and there are no instances where instructor would suggest moving logic or data to another class. The business-logic code driving functionality is cleanly separated from rendering, view-related code.


* Rare to see an instance property set [without assigning it some sort of default value](https://github.com/Rosebud303/Jeopardy/blob/master/src/DD.js#L8)

* Not 100% sold on extending the Round for your Daily Double...does the daily double clue need or use any of the methods in the round class? I think it more closely branches off of the clue class -- where daily doubles would also have a clue, an answer, a categoryID, etc. and only build on top of that to adjust the point value based on a player wage.

* Classes like [clues](https://github.com/Rosebud303/Jeopardy/blob/master/src/clues.js) should be singular, not plural. Each instance will represent a new Clue object, not an array of clues.


### Workflow
* [ ] Novice - The developer/team committed the code to version control in only a few commits. The evaluator cannot determine the evolution of the application.
* [ ] Advanced Beginner - The developer/team makes large commits covering multiple features that make it difficult for the evaluator to determine the evolution of the application. The team does not utilize a planning tool or equitable pairing practices. One or both members do not contribute meaningfully to the application.
* [x] Proficient - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.
* [ ] Exceptional - Meets all requirements for `Proficient`. In addition, the developer/team effectively uses Git branches and many small, atomic commits that document the evolution of their application with descriptive commit messages. The team displays good pairing practices (driver-navigator, dividing up work, etc) and utilizes some sort of planning tool (GitHub issues, Waffle, Trello, etc). The team develops a clear MVP (minimum viable product) and conducts a DTR (define the relationship). Both members contribute meaningfully to the application.

* Difficult to tell based on commits that Duy has mastered the learning goals. We understand you're pairing a lot together, but in the future make sure you are switching driver/navigator so that everyone has a chance to get some commits in. I understand there's often a lot of git issues/hiccups that make it easier to just work off of one person's machine. In that case, connect a keyboard and mouse to the machine so you can fairly alternate between committers. Employers will likely look at these stats too so you want to make sure they are representative of the amount of work you actually put in.