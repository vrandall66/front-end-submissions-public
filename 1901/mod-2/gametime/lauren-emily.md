# GameTime
* Students: Lauren & Emily
* Evaluator: Brittany
* Repo: [https://github.com/emilydittmer/gametime-jeopardy.git](https://github.com/emilydittmer/gametime-jeopardy.git)

### Functional Expectations

* [ ] Novice - Application is unplayable due to lack of functionality or broken logic. The majority of user stories are incomplete.
* [ x ] Advanced Beginner - Application has some missing functionality. Developers have implemented functionality for most of the user stories. There are 1 or more major bugs.
* [ ] Proficient - Application is fully playable. Developers have implemented functionality for all user stories.
* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, developers have implemented one or more extensions.

* Need to implement rounds and daily double




### UX/Accessibility

* [ ] Novice - The application is confusing or difficult to use.
* [ x ] Advanced Beginner - The application shows effort in the user experience, but the result is not effective. The evaluator has some difficulty using the application and may need assistance from developers.
* [ ] Proficient - The application is pleasant, logical, and easy to use. Developers use appropriate semantic elements in markup that allow for both mouse and keyboard navigation to all interactive elements.
* [ ] Exceptional -  Meets all expectations for `Proficient`.  In addition, developers implement attributes and ARIA labels where appropriate to allow for a better user experience with a screen reader. The application stands on its own to be used by the instructor _without_ guidance from the developers.

### User Interface

* [ ] Novice - Developers can integrate typography, color choices, and layout in ways that do not detract from legibility.
* [ x ] Advanced Beginner - Developers can apply fundamental design concepts with increased sensitivity that result in clear legibility but likely break in areas of layout or “noise”.
* [ ] Proficient - Developers can apply fundamental design concepts that demonstrates a thoughtful, purposeful, cohesive strategy that does not detract from legibility or overall design integrity.
* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, typography, color choices, and layout decisions are thoughtful and appropriate, and strongly enhance the layout and legibility of the design.

* Minimal, needs polishing and some effort put into typography/colors/CSS



### Testing

* [ ] Novice - There is little or no evidence of testing in this application. ESLint shows 10+ complaints.
* [ x ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.
* [ ] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.
* [ ] Exceptional - Meets all requires of `Proficient`. In addition, the test suite makes use of mocks and stubs when appropriate. ESLint shows 0 complaints.

* Tests like [this](https://github.com/emilydittmer/gametime-jeopardy/blob/master/test/Player-test.js#L13-L23) can be combined into a single it block that describes default instance properties. You probably also want to move that player instantiation to a `beforeEach` block so that you don't have to keep rewriting it in every test. I can tell based on your score increment/decrement tests that you could probably combine those two methods into a single one that says `updateScore` and takes in either a positive or negative number, rather than breaking it out to do addition vs. subraction. (You can always add a negative number and the ultimate effect would be that it does subtraction instead.)

* Would still like to see some expectations against spies being called - I see you started setting them up for the card tests (setup code looks good), but there aren't any assertions against those spies. Make sure you take this as an area of focus in your React apps!


### JavaScript Style & OOP

* [ ] Novice - Application is not separated into classes, or methods and properties are illogically assigned to classes. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Business-side logic and view-related code are not separated.
* [ ] Advanced Beginner - Application has a significant amount of duplication. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. 
* [ x ] Proficient - Application is thoughtfully put together with some duplication. Developers can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic. Business-logic code is mostly separated from view-related code. 
* [ ] Exceptional - Meets all requirements of `Proficient`. In addition, application has exceptionally well-factored code with little or no duplication. SRP (single responsibility principle) and DRY (don't repeat yourself) principles are utilized. There are _zero_ instances where an instructor would recommend taking a different approach. There are no instances where instructor would suggest moving logic or data to another class. The business-logic code driving functionality is cleanly separated from rendering, view-related code.

* Lots of hardcoding that is causing some verbose code (e.g. putting numbers in variable names rather than using arrays where appropriate). Room for plenty of refactoring, but nothing horrific.

### Workflow
* [ ] Novice - The developer/team committed the code to version control in only a few commits. The evaluator cannot determine the evolution of the application.
* [ ] Advanced Beginner - The developer/team makes large commits covering multiple features that make it difficult for the evaluator to determine the evolution of the application. The team does not utilize a planning tool or equitable pairing practices. One or both members do not contribute meaningfully to the application.
* [ x ] Proficient - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (Define the Relationship) that is linked in the README. Both members contribute meaningfully to the application.
* [ ] Exceptional - Meets all requirements for `Proficient`. In addition, the developer/team effectively uses Git branches and many small, atomic commits that document the evolution of their application with descriptive commit messages. The team displays good pairing practices (driver-navigator, dividing up work, etc) and utilizes some sort of planning tool (GitHub issues, Waffle, Trello, etc). 

* Based on commits, it looks like the distribution of work was pretty even though the line changes are a bit difficult to go by (nothing to worry about - just means that the bundle file was committed and severely inflated the line change counts for each contributor)

* Careful of slight variations in your commit messages -- they should all start with a capital letter, no punctuation, written in the imperative tense. Little consistency hiccups make the git history a bit more difficult to read, and many companies will be really strict about how you write your commit messages.