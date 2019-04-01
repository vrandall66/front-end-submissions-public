# GameTime
* Students: Katie & Hannah
* Evaluator: Brittany
* Repo: [https://github.com/kalex19/HH-KL-Family-Feud](https://github.com/kalex19/HH-KL-Family-Feud)

Very happy with the how the project turned out after the planning phase - it came together really well!


### Functional Expectations

* [ ] Novice - Application is unplayable due to lack of functionality or broken logic. The majority of user stories are incomplete.
* [ ] Advanced Beginner - Application has some missing functionality. Developers have implemented functionality for most of the user stories. There are 1 or more major bugs.
* [ x ] Proficient - Application is fully playable. Developers have implemented functionality for all user stories.
* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, developers have implemented one or more extensions.

* Resetting the answers to blank (weren't sure what happens with the screen reader in this scenario) 

* The inheritance piece you sent me looks accurate at a first glance, I'm also not 100% sure what issue you might have been running into when trying to implement that. I will count that as completed, as I can see you've demonstrated the ability to do it. The only thing I would change, as mentioned, is rewriting that one method name from `checkLr` to `check` so that it automatically overrides the behavior of the regular round's method.



### UX/Accessibility

* [ ] Novice - The application is confusing or difficult to use.
* [ ] Advanced Beginner - The application shows effort in the user experience, but the result is not effective. The evaluator has some difficulty using the application and may need assistance from developers.
* [ x ] Proficient - The application is pleasant, logical, and easy to use. Developers use appropriate semantic elements in markup that allow for both mouse and keyboard navigation to all interactive elements.
* [ ] Exceptional -  Meets all expectations for `Proficient`.  In addition, developers implement attributes and ARIA labels where appropriate to allow for a better user experience with a screen reader. The application stands on its own to be used by the instructor _without_ guidance from the developers.

### User Interface

* [ ] Novice - Developers can integrate typography, color choices, and layout in ways that do not detract from legibility.
* [ ] Advanced Beginner - Developers can apply fundamental design concepts with increased sensitivity that result in clear legibility but likely break in areas of layout or “noise”.
* [ ] Proficient - Developers can apply fundamental design concepts that demonstrates a thoughtful, purposeful, cohesive strategy that does not detract from legibility or overall design integrity.
* [ x ] Exceptional - Meets all expectations for `Proficient`. In addition, typography, color choices, and layout decisions are thoughtful and appropriate, and strongly enhance the layout and legibility of the design.

### Testing

* [ ] Novice - There is little or no evidence of testing in this application. ESLint shows 10+ complaints.
* [ ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.
* [ x ] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.
* [ ] Exceptional - Meets all requires of `Proficient`. In addition, the test suite makes use of mocks and stubs when appropriate. ESLint shows 0 complaints.

* Good job going back and getting some of that player/round testing in place, and adding some spy tests, though [this](https://github.com/kalex19/HH-KL-Family-Feud/blob/master/test/Round-test.js#L15-L21) could be done a bit more simply. You can pass in an array of method names you want to spy on as the second argument to `chai.spy.on()` instead of separating them all out onto their own line


### JavaScript Style & OOP

* [ ] Novice - Application is not separated into classes, or methods and properties are illogically assigned to classes. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Business-side logic and view-related code are not separated.
* [ ] Advanced Beginner - Application has a significant amount of duplication. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. 
* [ x ] Proficient - Application is thoughtfully put together with some duplication. Developers can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic. Business-logic code is mostly separated from view-related code. 
* [ ] Exceptional - Meets all requirements of `Proficient`. In addition, application has exceptionally well-factored code with little or no duplication. SRP (single responsibility principle) and DRY (don't repeat yourself) principles are utilized. There are _zero_ instances where an instructor would recommend taking a different approach. There are no instances where instructor would suggest moving logic or data to another class. The business-logic code driving functionality is cleanly separated from rendering, view-related code.

### Workflow
* [ ] Novice - The developer/team committed the code to version control in only a few commits. The evaluator cannot determine the evolution of the application.
* [ ] Advanced Beginner - The developer/team makes large commits covering multiple features that make it difficult for the evaluator to determine the evolution of the application. The team does not utilize a planning tool or equitable pairing practices. One or both members do not contribute meaningfully to the application.
* [ x ] Proficient - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (Define the Relationship) that is linked in the README. Both members contribute meaningfully to the application.
* [ ] Exceptional - Meets all requirements for `Proficient`. In addition, the developer/team effectively uses Git branches and many small, atomic commits that document the evolution of their application with descriptive commit messages. The team displays good pairing practices (driver-navigator, dividing up work, etc) and utilizes some sort of planning tool (GitHub issues, Waffle, Trello, etc). 

* It **looks** like there was an even distribution of work between the two partners, but it's difficult to tell because the commits that added the `main.bundle.js` file and `docs` directory created a pretty heft amount of line changes. Do reach out if you feel the division of labor was unfair in any way.

* Nice consistently formatted commit messages/readable git history