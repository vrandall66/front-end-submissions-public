# GameTime
* Game:
* Evaluator:

### Functional Expectations

* [ ] Novice - Application is unplayable due to lack of functionality or broken logic. The majority of user stories are incomplete.
* [ ] Advanced Beginner - Application has some missing functionality. Developers have implemented functionality for most of the user stories. There are 1 or more major bugs.
* [ ] Proficient - Application is fully playable. Developers have implemented functionality for all user stories.
* [ x ] Exceptional - Meets all expectations for `Proficient`. In addition, developers have implemented one or more extensions.

* + CSS animation


### UX/UI

* [ ] Novice - Developers can integrate typography, color choices, and layout in ways that do not detract from legibility.
* [ ] Advanced Beginner - Developers can apply fundamental design concepts with increased sensitivity that result in clear legibility but likely break in areas of layout or “noise”.
* [ x ] Proficient - Developers can apply fundamental design concepts that demonstrates a thoughtful, purposeful, cohesive strategy that does not detract from legibility or overall design integrity.
* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, typography, color choices, and layout decisions are thoughtful and appropriate, and strongly enhance the layout and legibility of the design.

* Really love the different take on the Game -- it gives you something unique for your portfolio that not every other Turing student is showing. 

* I like the fun witchy font for headings, but for buttons and elements I need to interact with, I'd stick to something a little more boring -- it can be a little overwhelming to try to read the text in that font unless it's really big and spare.

* Thank you for having hover states on your clickable elements!

* There are a *lot* of user interactions with wheel of fortune games, and they have a tendency to compete with each other on the page. I'd like a little more clarity around whether I'm supposed to be: spinning? picking a letter? buying a vowel? (can I even buy a vowel right now?) I think some disabled states would go a long way here -- making the buttons you **shouldnt** be interacting with a little less obvious until it's time to use them again 

### CSS/Sass Style

* [ ] Novice - There are several (10+) instances of duplication and one or two major bugs. Developers write code with unnecessary selectors or tags which do not increase clarity.
* [ ] Advanced Beginner - There is some duplication (5-10 instances) in the codebase. There may be one to two minor bugs. There may be some unncessary selectors or tags. Application adds organization for the whole stylesheet and within rules.
* [ ] Proficient - Application is thoughtfully put together with comments to help guide organization. There may be some duplication (fewer than 5 instances) present. Comments are present to assist with organization of code.
* [ x ] Exceptional - Meets all expectations for `Proficient`. The application has exceptionally well-factored CSS/Sass with all styles separated out into logical stylesheets. There are zero instances where an instructor would recommend taking a different approach.

* Nice use of variables and nesting and Ooooh some extends!! Variable names are solid (flexible enough not to have to change as the design changes but specific enough that I know what they represent)


### JavaScript Style & OOP

* [ ] Novice - Application is not separated into classes, or methods and properties are illogically assigned to classes. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Business-side logic and view-related code are not separated.
* [ ] Advanced Beginner - Application has a significant amount of duplication. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. 
* [ x ] Proficient - Application is thoughtfully put together with some duplication. Developers can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic. Business-logic code is mostly separated from view-related code. 
* [ ] Exceptional - Meets all requirements of `Proficient`. In addition, application has exceptionally well-factored code with little or no duplication. SRP (single responsibility principle) and DRY (don't repeat yourself) principles are utilized. There are _zero_ instances where an instructor would recommend taking a different approach. There are no instances where instructor would suggest moving logic or data to another class. The business-logic code driving functionality is cleanly separated from rendering, view-related code.

* [A good use-case for a for loop](https://github.com/aripp2/wheel-of-wizards/blob/master/src/Game.js#L19-L23) - you'll still use for loops once in a while!


* Is there a reason we're using [brack notation here](https://github.com/aripp2/wheel-of-wizards/blob/master/src/Puzzle.js#L10-L13) if we know all the names of the properties we're trying to access? I'd imagine dot notation would work just fine?

* The return statemetns in [this method](https://github.com/aripp2/wheel-of-wizards/blob/master/src/Round.js#L39-L46) are probably unecessary. It doesn't seem like you're doing anything with those return values, and you're actually returning an expression here...not a value. Would likely just end up returning `true` after that expression evaluates

* [This](https://github.com/aripp2/wheel-of-wizards/blob/master/src/Round.js#L56-L70) is a good use-case for a switch statement. Any time you have more than 2 possible conditions, I usually forgo the if/else syntax for a switch statement

* Alot of logic in your [BonusRound](https://github.com/aripp2/wheel-of-wizards/blob/master/src/BonusRound.js#L23-L27) duplicates code from your Round class. Remember extending a class means that you have access to all those methods by default, so we don't need to repeat them in our BonusRound class! You could completely delete that assignPuzzle method from BonusRound and it would work exactly the same.


### Testing

* [ ] Novice - There is little or no evidence of testing in this application. ESLint shows 10+ complaints.
* [ ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.
* [ x ] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.
* [ ] Exceptional - Meets all requires of `Proficient`. In addition, the test suite makes use of mocks and stubs when appropriate. ESLint shows 0 complaints.

* [WOW THATS A LOTTA SPIES](https://github.com/aripp2/wheel-of-wizards/blob/master/test/game-test.js#L14-L40) - I'm not sure I would pre-emptively spy on everything possible right off the bat. It might feel nice to know it's all taken care of, but it does make it a little more difficult to understand the intention/purpose of the spy if we just wipe out every domupdates method with a spy. I'd like to look at your spies and know exactly what to expect we're going to be spying on rather than having them all set up and only actually asserting against one of them

* Hmmm, I'm a little skeptical about this [join method](https://github.com/aripp2/wheel-of-wizards/blob/master/test/puzzle-test.js#L34) you're calling in the execution phase of your test here. That's something thats *not* happening in your application, and now you're asserting against code that you've written in your test file instead. We want to keep any sort of logic like this out of our tests so that we know we're always testing **only** what the app is doing and not something our test is doing.

* Good use of spies for your domUpdates, you can look into the `afterEach` or teardown phase to clean up your spies after each test runs. e.g. in the spies [here](https://github.com/aripp2/wheel-of-wizards/blob/master/test/round-test.js) it almost looks like you're call counts are continuously updating with each test block that finishes. We'd want to reset each spy to 0 and start with a clean slate for every it block so that our tests aren't dependent on each other. (e.g. if you change the order of your tests, would you still expect the `disableConsonants` method to have been called twice? or just once?)


### GitHub Collaboration/Workflow

* [ ] Novice - Developers do not tag instructors in the two required PRs by due dates listed in the project outline or tagged PR has fewer than 200 lines of code. The developer creating the PR does not summarize the changes or why the changes were made. Reviewers are not leaving line-by-line feedback/comments _or_ are merging the PR before changes are made.
* [ ] Advanced Beginner - Developers tag instructors in both required PRs by due dates _or_ in one of the two required. PR has less than the required lines of code in PR. Reviewers do not leave line-by-line feedback. May be merging PR before feedback is incorporated.
* [ x ] Proficient - Developers tag instructors in both required PRs by due dates. PR is over 100 lines of code. The developer creating the PR summarizes the changes made, why those changes were necessary, and asks for insights. Reviewers leave line-by-line comments/feedback and wait to merge PR until feedback is incorporated.
* [ ] Exceptional - Meets all expectations for `Proficient`. The feedback is both kind _and_ insightful. There may be numerous threads of conversation where developers go back and forth to find the best solution to the problems they are solving together.

### Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.
* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 
* [ ] Proficient - Everyone in the group has an opporunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.
* [ ] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.
