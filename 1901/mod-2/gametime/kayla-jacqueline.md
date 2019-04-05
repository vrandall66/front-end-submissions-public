# GameTime
* Students: Kayla & Jacqueline
* Evaluator: Brittany
* Repo: [https://github.com/KaylaLawson/Jeopardy-JK](https://github.com/KaylaLawson/Jeopardy-JK)

* Overall, not bad -- I would consider this a passing project where most of the learning goals were met. I would recommend doing a bit more external research on inheritance with OOP, as that's the only area I'm still seeing some subtle misconceptions. 



### Functional Expectations

* [ ] Novice - Application is unplayable due to lack of functionality or broken logic. The majority of user stories are incomplete.
* [ x ] Advanced Beginner - Application has some missing functionality. Developers have implemented functionality for most of the user stories. There are 1 or more major bugs.
* [ ] Proficient - Application is fully playable. Developers have implemented functionality for all user stories.
* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, developers have implemented one or more extensions.


* The implementation of Daily Double is just slightly off -- it probably wouldn't want to extend the Round class. Instead, you'd likely have something like a `Clue` or `Question` class that just holds on to the clue text, the correct answer, and the point value. The Daily Double class would inherit those properties, and maybe differ only slightly by having an `acceptWager` method that allows a user to change the point value of that clue. Right now the DD is inheriting a bit too many unecessary things from the Round class.


### UX/Accessibility

* [ ] Novice - The application is confusing or difficult to use.
* [ ] Advanced Beginner - The application shows effort in the user experience, but the result is not effective. The evaluator has some difficulty using the application and may need assistance from developers.
* [ x ] Proficient - The application is pleasant, logical, and easy to use. Developers use appropriate semantic elements in markup that allow for both mouse and keyboard navigation to all interactive elements.
* [ ] Exceptional -  Meets all expectations for `Proficient`.  In addition, developers implement attributes and ARIA labels where appropriate to allow for a better user experience with a screen reader. The application stands on its own to be used by the instructor _without_ guidance from the developers.

* Make sure things that you *cant* click on denote that. Make them look a bit more disabled

* Glad to see some font pairing, but the cursive is a little difficult to read

* Would like it to be a bit more obvious when a user gets a question right or wrong


### User Interface

* [ ] Novice - Developers can integrate typography, color choices, and layout in ways that do not detract from legibility.
* [ ] Advanced Beginner - Developers can apply fundamental design concepts with increased sensitivity that result in clear legibility but likely break in areas of layout or “noise”.
* [ x ] Proficient - Developers can apply fundamental design concepts that demonstrates a thoughtful, purposeful, cohesive strategy that does not detract from legibility or overall design integrity.
* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, typography, color choices, and layout decisions are thoughtful and appropriate, and strongly enhance the layout and legibility of the design.


### Testing

* [ ] Novice - There is little or no evidence of testing in this application. ESLint shows 10+ complaints.
* [ ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.
* [ x ] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.
* [ ] Exceptional - Meets all requires of `Proficient`. In addition, the test suite makes use of mocks and stubs when appropriate. ESLint shows 0 complaints.

* Nice use of spies in your round test [here](https://github.com/KaylaLawson/Jeopardy-JK/blob/master/test/Round-test.js#L79) and setup of mock data [here](https://github.com/KaylaLawson/Jeopardy-JK/blob/master/test/Round-test.js#L50-L51)

* Probably don't need to invoke [changePlayer](https://github.com/KaylaLawson/Jeopardy-JK/blob/master/test/Game-test.js#L43-L44) twice here -- it doesn't give you any added assurance of your project working. Once is enough :) 

* You probably don't need to be instantiating an entire game [here](https://github.com/KaylaLawson/Jeopardy-JK/blob/master/test/Round-test.js#L55)? Doesn't look like you're using that game variable anywhere. 


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



* Division of work looks even, for issue filing, I would file one issue per task rather than a single issue that lists all of them (like you have [here](https://github.com/KaylaLawson/Jeopardy-JK/issues/23))

* Be sure to have consistency in the formatting of your commit messages so that the git history is as readable as possible (e.g. commits should be written like 'Add bonus round functionality' rather than just 'bonus round')