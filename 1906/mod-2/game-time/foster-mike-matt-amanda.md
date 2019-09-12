# GameTime
* Game: [J](https://github.com/mschneider247/quest-to-jeff)
* Evaluator:

### Functional Expectations

* [ ] Novice - Application is unplayable due to lack of functionality or broken logic. The majority of user stories are incomplete.
* [x] Advanced Beginner - Application has some missing functionality. Developers have implemented functionality for most of the user stories. There are 1 or more major bugs.
* [ ] Proficient - Application is fully playable. Developers have implemented functionality for all user stories.
* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, developers have implemented one or more extensions.


### UI/UX

* [ ] Novice - Developers can integrate typography, color choices, and layout in ways that do not detract from legibility.
* [ ] Advanced Beginner - Developers can apply fundamental design concepts with increased sensitivity that result in clear legibility but likely break in areas of layout or “noise”.
* [x] Proficient - Developers can apply fundamental design concepts that demonstrates a thoughtful, purposeful, cohesive strategy that does not detract from legibility or overall design integrity.
* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, typography, color choices, and layout decisions are thoughtful and appropriate, and strongly enhance the layout and legibility of the design.

* Very nice background, such a cool design element!! Way to go on that.

* As mentioned during check-in, heirarchy of what's important can be denoted a little better through your font styling. Overall not too difficult to use but definitely takes a minute to orient yourself. 

### CSS/Sass Style

* [ ] Novice - There are several (10+) instances of duplication and one or two major bugs. Developers write code with unnecessary selectors or tags which do not increase clarity.
* [ ] Advanced Beginner - There is some duplication (5-10 instances) in the codebase. There may be one to two minor bugs. There may be some unncessary selectors or tags. Application adds organization for the whole stylesheet and within rules.
* [ ] Proficient - Application is thoughtfully put together with comments to help guide organization. There may be some duplication (fewer than 5 instances) present. Comments are present to assist with organization of code.
* [ ] Exceptional - Meets all expectations for `Proficient`. The application has exceptionally well-factored CSS/Sass with all styles separated out into logical stylesheets. There are zero instances where an instructor would recommend taking a different approach.


### JavaScript Style & OOP

* [ ] Novice - Application is not separated into classes, or methods and properties are illogically assigned to classes. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Business-side logic and view-related code are not separated.
* [x] Advanced Beginner - Application has a significant amount of duplication. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. 
* [x] Proficient - Application is thoughtfully put together with some duplication. Developers can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic. Business-logic code is mostly separated from view-related code. 
* [ ] Exceptional - Meets all requirements of `Proficient`. In addition, application has exceptionally well-factored code with little or no duplication. SRP (single responsibility principle) and DRY (don't repeat yourself) principles are utilized. There are _zero_ instances where an instructor would recommend taking a different approach. There are no instances where instructor would suggest moving logic or data to another class. The business-logic code driving functionality is cleanly separated from rendering, view-related code.


* There are still some gaps in OOP understanding when it comes to what behaviors exist where. We discussed during check-in something like the player's score --- if the player class holds onto the score as their instance property, they should be the ones updating it. Right now your clue class is manually updating the player score rather than letting the player class handle its own state. I recall during that check-in that Mike articulated this approach perfectly, I'm curious why that strategy wasn't taken.

* It seems you have some duplicate methods - e.g. `checkDailyDouble` on the clue and the round class -- this is a little confusing and makes it hard to understand your separation of responsibilities between classes.

### Testing

* [ ] Novice - There is little or no evidence of testing in this application. ESLint shows 10+ complaints.
* [x] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.
* [ ] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.
* [ ] Exceptional - Meets all requires of `Proficient`. In addition, the test suite makes use of mocks and stubs when appropriate. ESLint shows 0 complaints.

* You shouldn't need to be doing [this much setup](https://github.com/mschneider247/quest-to-jeff/blob/master/test/Clue-test.js#L12-L17) to test your clue class. The point of classes is that each of them can mostly stand on their own in isolation to work and be tested. In this instance, you should just have to spin up a new instance of a clue, and test: default properties, the `checkAnswer`  and `checkDailyDouble` method. The `updatePlayerScore` method should exist on your player class, not your clue class.

* Manually set values for [these arguments](https://github.com/mschneider247/quest-to-jeff/blob/master/test/Clue-test.js#L17) like `new Clue(clueObject, false)` rather than trying to instantiate a round and game to do all that heavy lifting. That will reduce the amount of setup code you're doing here.

* You should at the very least be testing default properties for your Player class, even if it's small and simple!

* Missing a lot of method tests due to not spying on domUpdate calls -- spies are something you'll need to be doing in your solo projects and in Mod 3 so please get some practice with that!



### GitHub Collaboration/Workflow

* [ ] Novice - Developers do not tag instructors in the two required PRs by due dates listed in the project outline or tagged PR has fewer than 200 lines of code. The developer creating the PR does not summarize the changes or why the changes were made. Reviewers are not leaving line-by-line feedback/comments _or_ are merging the PR before changes are made.
* [x] Advanced Beginner - Developers tag instructors in both required PRs by due dates _or_ in one of the two required. PR has less than the required lines of code in PR. Reviewers do not leave line-by-line feedback. May be merging PR before feedback is incorporated.
* [ ] Proficient - Developers tag instructors in both required PRs by due dates. PR is over 100 lines of code. The developer creating the PR summarizes the changes made, why those changes were necessary, and asks for insights. Reviewers leave line-by-line comments/feedback and wait to merge PR until feedback is incorporated.
* [ ] Exceptional - Meets all expectations for `Proficient`. The feedback is both kind _and_ insightful. There may be numerous threads of conversation where developers go back and forth to find the best solution to the problems they are solving together.

- Make sure to keep your commit messages active, not passive ("Remove line", not "Removed line")

- You have some pretty heavy commits in here. Make sure to opt on the side of keeping your commits small and organized -- rather than committing after fixing several bugs, commit after each bug gets fixed

- Looking at the insights, it seems like Matt had nearly all of the contributions, in terms of line numbers. I know you were coauthoring a lot of commits -- this can make it hard to accurately determine how much everyone contributed. It looks like Foster has a low number relative to other group members, and I know Michael is having issues with his account. Make sure that if you're working as a driver-navigator, you regularly switch who is driving to keep the commits evenly distributed.

- We were only tagged in one PR -- make sure you're checking the required number of PRs so we can give you enough code review

### Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.
* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 
* [x] Proficient - Everyone in the group has an opporunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.
* [ ] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.

- they have slides talking about their planning phase 
- utilized GH issues 
- Presentation could have been a little more polished, but they had a good demo and sldie structure 
- Didn't get all the way through round three 
