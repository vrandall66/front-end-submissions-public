# Game Time
* Students: Gabe and Niraj
* Evaluator: Robbie

Comments:
* This project is barely passing - testing is pretty bare bones and features are very buggy. Marking this project as "passing with concern".
* it seems like there was time spent on UI that would have been better spent on finishing features and testing more thoroughly.

### Functional Expectations

* [ ] Novice - Application is unplayable due to lack of functionality or broken logic.
* [X] Advanced Beginner - Application has some missing functionality but no bugs or broken functionality.
* [ ] Proficient - Application is fully playable and meets all requirements of the spec.
* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, the application exceeds the expectations set by instructors.

- There are a few bugs as you play the game
- Bonus round is functional, but not styled and as a result a little difficult to play

### User Interface

* [ ] Novice - The application is confusing or difficult to use.
* [ ] Advanced Beginner - The application shows effort in the interface, but the result is not effective. The evaluator has some difficulty using the application when reviewing the features in the user stories.
* [X] Proficient - The application has many strong pages/interactions, but a few holes in lesser-used functionality.
* [ ] Exceptional -  Meets all expectations for `Proficient`. In addition, the application is pleasant, logical, and easy to use. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer.

- I like the overall theme, it's a bit retro
- The background is a little distracting and makes the contrast against the puzzle a little difficult to read
- Would be nice to center the puzzle more, especially for short puzzles
- Need indication of which player's turn it is

### Testing

* [ ] Novice - There is little or no evidence of testing in this application. ESLint shows 10+ complaints.
* [ ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.
* [X] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.
* [ ] Exceptional - Meets all requires of `Proficient`. In addition, the test suite makes use of mocks and stubs when appropriate. ESLint shows 0 complaints.

- Some methods are still not tested (Bonus is not tested) - we will expect that **every** method in your following projects are tested. Testing is no longer a nice-to-have in projects.
- Was Novice due to missing tests for major classes, but moved to Proficient after some revisions (but just barely)
- Good job using the `beforeEach` hook to keep some tests DRY, for instance in the `Wheel` test
- Good job testing and making an assertion with the spy [here](https://github.com/niroz11/wheel-of-fortune/blob/master/test/Round-test.js#L34)

### JavaScript Style & OOP

* [ ] Novice - Your client-side application does not function. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Application is not separated into classes, or methods and properties are illogically assigned to classes. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Business-side logic and view-related code is not separated.
* [ ] Advanced Beginner - Your application has a significant amount of duplication and one or more major bugs. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. There are one or more major bugs.
* [X] Proficient - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.
* [ ] Exceptional - Meets all requirements of `Proficient`. In addition, application has exceptionally well-factored code with little or no duplication. SRP (single responsibility principle) and DRY (don't repeat yourself) principles are utilized. There are _zero_ instances where an instructor would recommend taking a different approach. Application is organized into classes (and correctly uses inheritance) and there are no instances where instructor would suggest moving logic or data to another class. The business-logic code driving functionality is cleanly separated from rendering, view-related code.

- At the time of eval, there was still some jQuery in the `Game` class, but this was moved to domUpdates, good job
- The `parseData` method in `Game` is doing way more than parsing data, try to think of another name to describe that method's role
- Right now, `Bonus` is living inside of `Round` - every class should have its own file even if a class is inheriting from the other
- Seems like this [chunk of code](https://github.com/niroz11/wheel-of-fortune/blob/master/src/round.js#L64-L70) was lifted from Stack Overflow - if I asked to you to describe to me exactly how that code is working, would you be able to tell me? Next time, make something simple yourself even if it doesn't work perfectly.
- Good job keeping the `Game` class relatively small and giving the other classes control over their responsibilities

### Workflow
* [ ] Novice - The developer/team committed the code to version control in only a few commits. The evaluator cannot determine the evolution of the application.
* [ ] Advanced Beginner - The developer/team makes large commits covering multiple features that make it difficult for the evaluator to determine the evolution of the application. The team does not utilize a planning tool or equitable pairing practices. One or both members do not contribute meaningfully to the application.
* [X] Proficient - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.
* [ ] Exceptional - Meets all requirements for `Proficient`. In addition, the developer/team effectively uses Git branches and many small, atomic commits that document the evolution of their application with descriptive commit messages. The team displays good pairing practices (driver-navigator, dividing up work, etc) and utilizes some sort of planning tool (GitHub issues, Waffle, Trello, etc). The team develops a clear MVP (minimum viable product) and conducts a DTR (define the relationship). Both members contribute meaningfully to the application.

- How did the `.gitignore` get changed to something completely different from the game time starter kit? You have committed `node_modules`, which has added a lot of unnecessary bloat to your repo. Do not commit `node_modules` in the future.
- It seems like one person is on tabs and one person is using spaces for their text editors, and it is causing some weirdness in indentation. Overall, indentation across the project is very sloppy. This is something that employers will see and think you do not have attention to detail, which is important in coding. Also, add spacing between methods in classes.
