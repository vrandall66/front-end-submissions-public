# GameTime
* Game: [WOF](https://github.com/JEduardoRJx/game-time.git)
* Evaluator:

### Functional Expectations

* [ ] Novice - Application is unplayable due to lack of functionality or broken logic. The majority of user stories are incomplete.
* [ ] Advanced Beginner - Application has some missing functionality. Developers have implemented functionality for most of the user stories. There are 1 or more major bugs.
* [x] Proficient - Application is fully playable. Developers have implemented functionality for all user stories.
* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, developers have implemented one or more extensions.

* Bonus round is missing tests and needs refactoring to work/test properly, but OK

### UI/UX

* [ ] Novice - Developers can integrate typography, color choices, and layout in ways that do not detract from legibility.
* [x] Advanced Beginner - Developers can apply fundamental design concepts with increased sensitivity that result in clear legibility but likely break in areas of layout or “noise”.
* [ ] Proficient - Developers can apply fundamental design concepts that demonstrates a thoughtful, purposeful, cohesive strategy that does not detract from legibility or overall design integrity.
* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, typography, color choices, and layout decisions are thoughtful and appropriate, and strongly enhance the layout and legibility of the design.

* VERY CREEPY!!!! I am legit scared looking at this, it's great. The CSS fade transition when starting a game is awesome for this theme. Normally I recommend making your CSS animations as fast and subtle as possible, but having this super slow fade really adds to the creepiness. 

* UX only took a little bit of getting used to before I knew my way around. Good job at keeping relevant/possible interactions at the forefront, and otthers in the background. I think something that would help further would be to contain related elements together a bit. e.g. each of your player name/score elements are pretty far apart horizontally. If we could cluster those together a bit closer, and maybe give them a container element with a subtle background or border, that might help me mentally group the elements on the page a little better.

* The transparancies on the `Solve Puzzle` button made it a little unclear that it was interactible 


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

* Make sure you delete any files that aren't doing anything...if employers are taking a really quick look at your file structure they might be misled about your classes/codebase organization just by seeing how many files there are rather than how many are actually doing something. Also get rid of any commented out code. As a first impression, the codebase looks a little sloppy due to these things.

* Mostly a solid representation of OOP skills although like many, I feel the Turn class is doing a bit more than it should compared to that Player class. Make these methods a bit smaller if possible and move them to a more appropriate place.

### Testing

* [ ] Novice - There is little or no evidence of testing in this application. ESLint shows 10+ complaints.
* [ ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.
* [x] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.
* [ ] Exceptional - Meets all requires of `Proficient`. In addition, the test suite makes use of mocks and stubs when appropriate. ESLint shows 0 complaints.

* [This](https://github.com/JEduardoRJx/game-time/blob/master/test/game-test.js#L9) shouldn't be necessary, and I'm interested if it's actually causing problems rather than helping. It could potentially be overriding your actual `domUpdates` object which would be clearing out any of it's methods that you want to be spying on.

* I would break [these](https://github.com/JEduardoRJx/game-time/blob/master/test/turn-test.js#L57-L60) into separate tests - one for when the puzzle is solved correctly/one for when its not. Any time you have conditional logic that changes the state of your app in a different way, have separate it blocks for both conditions.

* You shouldnt have to do [quite so much setup code](https://github.com/JEduardoRJx/game-time/blob/master/test/turn-test.js#L21-L30) -- pass in an object literal that looks like a round to your Turn class when you instantiate it rather than spinning up an entire game instance and round instance to stub that functionality. If your classes are truly independent of each other, you shouldn't need to spin up all these other class instances just to test one class.

* Many method tests missing due to not breaking out jQuery dom manipulation well enough in classes


### GitHub Collaboration/Workflow

* [ ] Novice - Developers do not tag instructors in the two required PRs by due dates listed in the project outline or tagged PR has fewer than 200 lines of code. The developer creating the PR does not summarize the changes or why the changes were made. Reviewers are not leaving line-by-line feedback/comments _or_ are merging the PR before changes are made.
* [ ] Advanced Beginner - Developers tag instructors in both required PRs by due dates _or_ in one of the two required. PR has less than the required lines of code in PR. Reviewers do not leave line-by-line feedback. May be merging PR before feedback is incorporated.
* [x] Proficient - Developers tag instructors in both required PRs by due dates. PR is over 100 lines of code. The developer creating the PR summarizes the changes made, why those changes were necessary, and asks for insights. Reviewers leave line-by-line comments/feedback and wait to merge PR until feedback is incorporated.
* [ ] Exceptional - Meets all expectations for `Proficient`. The feedback is both kind _and_ insightful. There may be numerous threads of conversation where developers go back and forth to find the best solution to the problems they are solving together.

- Eduardo, it looks like you have a low number of contributinos compared to the rest of the team. I know you all did a fiar amount of co-authoring, but the line contributions only show up on the driver's account. If you're using a driver-navigator workflow, make sure you alternate who is driving reguarly, so that your contributinos show up accutately on your account 

- The PR you submitted for review had enough changes that we could give some real code review, good job here

- Break down your commits a bit more. You have one that encompasses nearly all the bonus round functionality. This can get broken down into commits for methods and properties if you wanted. Think about what would be helpful if you had to revert a fiel back to a commit. Would you want to have to roll back all of your bonus round functionality? 

### Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.
* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 
* [ ] Proficient - Everyone in the group has an opporunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.
* [x] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.

- Nice explanation of the way the game works 
- Solid demo 
- Nice presentation structure
- Make issues that represent the future changes you would make 
- Great presentation!
