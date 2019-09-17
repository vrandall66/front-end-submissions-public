# GameTime
* Game: [WOF](https://github.com/peeratmac/game-time)
* Evaluator:

### Functional Expectations

* [ ] Novice - Application is unplayable due to lack of functionality or broken logic. The majority of user stories are incomplete.
* [x] Advanced Beginner - Application has some missing functionality. Developers have implemented functionality for most of the user stories. There are 1 or more major bugs.
* [ ] Proficient - Application is fully playable. Developers have implemented functionality for all user stories.
* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, developers have implemented one or more extensions.

* Missing use-case for inheritance

### UI/UX

* [ ] Novice - Developers can integrate typography, color choices, and layout in ways that do not detract from legibility.
* [ ] Advanced Beginner - Developers can apply fundamental design concepts with increased sensitivity that result in clear legibility but likely break in areas of layout or “noise”.
* [x] Proficient - Developers can apply fundamental design concepts that demonstrates a thoughtful, purposeful, cohesive strategy that does not detract from legibility or overall design integrity.
* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, typography, color choices, and layout decisions are thoughtful and appropriate, and strongly enhance the layout and legibility of the design.

- Fonts are a little hard to see from far away, but the overall UI looks nice. Good color mathcing, nice pixel fonts in terms of design 

- Like the arcade-stlye layout 

### CSS/Sass Style

* [ ] Novice - There are several (10+) instances of duplication and one or two major bugs. Developers write code with unnecessary selectors or tags which do not increase clarity.
* [ ] Advanced Beginner - There is some duplication (5-10 instances) in the codebase. There may be one to two minor bugs. There may be some unncessary selectors or tags. Application adds organization for the whole stylesheet and within rules.
* [ ] Proficient - Application is thoughtfully put together with comments to help guide organization. There may be some duplication (fewer than 5 instances) present. Comments are present to assist with organization of code.
* [ ] Exceptional - Meets all expectations for `Proficient`. The application has exceptionally well-factored CSS/Sass with all styles separated out into logical stylesheets. There are zero instances where an instructor would recommend taking a different approach.


### JavaScript Style & OOP

* [ ] Novice - Application is not separated into classes, or methods and properties are illogically assigned to classes. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Business-side logic and view-related code are not separated.
* [ ] Advanced Beginner - Application has a significant amount of duplication. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. 
* [x] Proficient - Application is thoughtfully put together with some duplication. Developers can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic. Business-logic code is mostly separated from view-related code. 
* [ ] Exceptional - Meets all requirements of `Proficient`. In addition, application has exceptionally well-factored code with little or no duplication. SRP (single responsibility principle) and DRY (don't repeat yourself) principles are utilized. There are _zero_ instances where an instructor would recommend taking a different approach. There are no instances where instructor would suggest moving logic or data to another class. The business-logic code driving functionality is cleanly separated from rendering, view-related code.

* Overall pretty solid separation of responsibilities between your classes (I still believe your Round class is doing a bit extra that could be offloaded to your player instead) but OOP fundamentals have been demonstrated just fine

* [Hmmm whats this line of code doing? Nothing?](https://github.com/peeratmac/game-time/blob/master/src/Player.js#L26)

* I would expect a method called [getWinnerThisRound](https://github.com/peeratmac/game-time/blob/master/src/Game.js#L47-L56) to do something like return a player's name/score. I'm a little confused by what we're doing with the map here. Maybe the name of this method just needs to change to be a little more explicit about what the logic is doing?


### Testing

* [ ] Novice - There is little or no evidence of testing in this application. ESLint shows 10+ complaints.
* [x] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.
* [ ] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.
* [ ] Exceptional - Meets all requires of `Proficient`. In addition, the test suite makes use of mocks and stubs when appropriate. ESLint shows 0 complaints.

* I'm not sure how [this test](https://github.com/peeratmac/game-time/blob/master/test/Game-test.js#L56-L70) verifies that your game is determining the winner for each round. You are passing through player 0 to your method call and then expecting your players array to be stored in `game.players`? Is there something significant about the sort order of the players here that's verifying which player is the winner? I would not be able to reimplement the functionality of `getWinnerThisRound` simply by looking at this test. (That should always be the goal!)

* I think we have a few too many [assertions](https://github.com/peeratmac/game-time/blob/master/test/Player-test.js#L23-L31) here. They seem a bit random as well. I would have 1 it block that tests that `updateCurrentRoundMoney` changes a single players value, and another it block that tests a call to `updateTotalMoney` for a single player. Working with two different players and exercises two different methods in a single it block makes it a little hard to follow.

* Can we get any more specific with the assertions [here](https://github.com/peeratmac/game-time/blob/master/test/Puzzle-test.js)? Rather than just testing if something is an array or object? Again, I feel like I would not be able to re-implement your Puzzle class based on reading your tests here.

* Make sure to leverage spies in your solo projects to get that practice down before Mod 3!!

### GitHub Collaboration/Workflow

* [ ] Novice - Developers do not tag instructors in the two required PRs by due dates listed in the project outline or tagged PR has fewer than 200 lines of code. The developer creating the PR does not summarize the changes or why the changes were made. Reviewers are not leaving line-by-line feedback/comments _or_ are merging the PR before changes are made.
* [ ] Advanced Beginner - Developers tag instructors in both required PRs by due dates _or_ in one of the two required. PR has less than the required lines of code in PR. Reviewers do not leave line-by-line feedback. May be merging PR before feedback is incorporated.
* [x] Proficient - Developers tag instructors in both required PRs by due dates. PR is over 100 lines of code. The developer creating the PR summarizes the changes made, why those changes were necessary, and asks for insights. Reviewers leave line-by-line comments/feedback and wait to merge PR until feedback is incorporated.
* [ ] Exceptional - Meets all expectations for `Proficient`. The feedback is both kind _and_ insightful. There may be numerous threads of conversation where developers go back and forth to find the best solution to the problems they are solving together.

- Make sure you're keeping your commits frequent; some of the styling ones are getting to be on the longer side 
- PR formatting and workflow looks good 
- Peerat it looks like you have a few huge commits, I'm not positive where exactly these were comoing from, but make sure you aren't committing unnescessary things 

### Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.
* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 
* [x] Proficient - Everyone in the group has an opporunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.
* [ ] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.

- Reflected on the challenges of working remotely 
  - Also the learning opportunities it presented 
- What were the reasons for the UI or class structure switch ups 
- Good job touching on extra functionality you would implement -- make sure they're represented in GH issues!
