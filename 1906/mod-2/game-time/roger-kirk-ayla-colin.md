# GameTime
* Game: [FF](https://github.com/KVeitch/FamilyFeud)
* Evaluator:

### Functional Expectations

* [ ] Novice - Application is unplayable due to lack of functionality or broken logic. The majority of user stories are incomplete.
* [ ] Advanced Beginner - Application has some missing functionality. Developers have implemented functionality for most of the user stories. There are 1 or more major bugs.
* [x] Proficient - Application is fully playable. Developers have implemented functionality for all user stories.
* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, developers have implemented one or more extensions.


### UI/UX

* [ ] Novice - Developers can integrate typography, color choices, and layout in ways that do not detract from legibility.
* [ ] Advanced Beginner - Developers can apply fundamental design concepts with increased sensitivity that result in clear legibility but likely break in areas of layout or “noise”.
* [ ] Proficient - Developers can apply fundamental design concepts that demonstrates a thoughtful, purposeful, cohesive strategy that does not detract from legibility or overall design integrity.
* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, typography, color choices, and layout decisions are thoughtful and appropriate, and strongly enhance the layout and legibility of the design.

- Nice animations with the appended HTML 



### CSS/Sass Style

* [ ] Novice - There are several (10+) instances of duplication and one or two major bugs. Developers write code with unnecessary selectors or tags which do not increase clarity.
* [ ] Advanced Beginner - There is some duplication (5-10 instances) in the codebase. There may be one to two minor bugs. There may be some unncessary selectors or tags. Application adds organization for the whole stylesheet and within rules.
* [ ] Proficient - Application is thoughtfully put together with comments to help guide organization. There may be some duplication (fewer than 5 instances) present. Comments are present to assist with organization of code.
* [ ] Exceptional - Meets all expectations for `Proficient`. The application has exceptionally well-factored CSS/Sass with all styles separated out into logical stylesheets. There are zero instances where an instructor would recommend taking a different approach.


### JavaScript Style & OOP

* [ ] Novice - Application is not separated into classes, or methods and properties are illogically assigned to classes. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Business-side logic and view-related code are not separated.
* [ ] Advanced Beginner - Application has a significant amount of duplication. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. 
* [] Proficient - Application is thoughtfully put together with some duplication. Developers can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic. Business-logic code is mostly separated from view-related code. 
* [x] Exceptional - Meets all requirements of `Proficient`. In addition, application has exceptionally well-factored code with little or no duplication. SRP (single responsibility principle) and DRY (don't repeat yourself) principles are utilized. There are _zero_ instances where an instructor would recommend taking a different approach. There are no instances where instructor would suggest moving logic or data to another class. The business-logic code driving functionality is cleanly separated from rendering, view-related code.

* [This](https://github.com/KVeitch/FamilyFeud/blob/master/src/fastMoneyRound.js#L19) is a bit too complex/too much code for a ternary - i'd switch this to an if/else 

* Let's move this [jQuery](https://github.com/KVeitch/FamilyFeud/blob/master/src/turn.js#L13) outta here so that we can test this method!

* Overall nice tiny methods with small responsibilities and good organization of behaviors/information


### Testing

* [ ] Novice - There is little or no evidence of testing in this application. ESLint shows 10+ complaints.
* [ ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.
* [x] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.
* [ ] Exceptional - Meets all requires of `Proficient`. In addition, the test suite makes use of mocks and stubs when appropriate. ESLint shows 0 complaints.

* No need to instantiate and test against [two players](https://github.com/KVeitch/FamilyFeud/blob/master/test/player-test.js#L7-L19) in this test file. Just one will do :)

* I'm curious about trying to spy on your Turn methods [here](https://github.com/KVeitch/FamilyFeud/blob/master/test/turn-test.js#L14)? If you are trying to test your Turn class, you would actually want these to run and assert against their behavior, not just verify that they were called.

* You should be able to rip [this out](https://github.com/KVeitch/FamilyFeud/blob/master/test/turn-test.js#L16-L17) if you set up all your spies correctly on your DOM manipulation. It seems like this can be an area of practice for your solo projects. Make sure everyone fully understands how to implement spies!

### GitHub Collaboration/Workflow

* [ ] Novice - Developers do not tag instructors in the two required PRs by due dates listed in the project outline or tagged PR has fewer than 200 lines of code. The developer creating the PR does not summarize the changes or why the changes were made. Reviewers are not leaving line-by-line feedback/comments _or_ are merging the PR before changes are made.
* [x] Advanced Beginner - Developers tag instructors in both required PRs by due dates _or_ in one of the two required. PR has less than the required lines of code in PR. Reviewers do not leave line-by-line feedback. May be merging PR before feedback is incorporated.
* [ ] Proficient - Developers tag instructors in both required PRs by due dates. PR is over 100 lines of code. The developer creating the PR summarizes the changes made, why those changes were necessary, and asks for insights. Reviewers leave line-by-line comments/feedback and wait to merge PR until feedback is incorporated.
* [ ] Exceptional - Meets all expectations for `Proficient`. The feedback is both kind _and_ insightful. There may be numerous threads of conversation where developers go back and forth to find the best solution to the problems they are solving together.
- Ayla was your brother commenting on PRs?
- Conributinos from Colin and Roger are on the lower side compared to other gruop members; make sure that if you're driving and navigating, you keep alternate who the driver is so that contributions are evely distributed. Co-authoring doens't totally share them across co-authors
- Capiatlize the start of commit messages, and make sure they're written in the active / imperative voice 
- On the whole, most commits look like they're of a pretty good size, not too large 
- PRs to us could have been bigger, there wasn't always a ton of code to review

### Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.
* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 
* [x] Proficient - Everyone in the group has an opporunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.
* [ ] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.

- Good demo 
- Appreciate the honesty about challenges and testing coverage -- make sure this is in the repo as an issue 
- Solid division of labor in the presentation 
