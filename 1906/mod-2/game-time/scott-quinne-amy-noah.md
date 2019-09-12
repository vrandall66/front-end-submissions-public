# GameTime
* Game: [FF](https://github.com/sschipke/gameTime)
* Evaluator:

### Functional Expectations

* [ ] Novice - Application is unplayable due to lack of functionality or broken logic. The majority of user stories are incomplete.
* [ ] Advanced Beginner - Application has some missing functionality. Developers have implemented functionality for most of the user stories. There are 1 or more major bugs.
* [ ] Proficient - Application is fully playable. Developers have implemented functionality for all user stories.
* [x] Exceptional - Meets all expectations for `Proficient`. In addition, developers have implemented one or more extensions.


### UI/UX

* [ ] Novice - Developers can integrate typography, color choices, and layout in ways that do not detract from legibility.
* [ ] Advanced Beginner - Developers can apply fundamental design concepts with increased sensitivity that result in clear legibility but likely break in areas of layout or “noise”.
* [ ] Proficient - Developers can apply fundamental design concepts that demonstrates a thoughtful, purposeful, cohesive strategy that does not detract from legibility or overall design integrity.
* [x] Exceptional - Meets all expectations for `Proficient`. In addition, typography, color choices, and layout decisions are thoughtful and appropriate, and strongly enhance the layout and legibility of the design.

* B-e-a-utiful UI! One of the best I've seen from Mod 2ers. Love the bold background and large text. Font pairings look great. Definitely be showing this off at code fair!!! Great disabled/active/hover states on your clickable elements. Love the subtle CSS transition in the background as the game gets started to bring the UI into place, while we read the instructiosn in the popup window.

* One thing I mighttttttt do - is some content alignment on your theme. I like the git-style action labels for interacting with the app, but I think they'd work better if the dataset was full of tech/programming related questions. e.g. if you could find developer surveys (they do one on JS every year) that had questions like 'Name the top three most used git commands' or 'Name a framework you might develop a front-end application in', the git labels would make a little more sense here. Obviously changing your dataset wasn't an option based on the spec, but maybe for a future iteration. It's a good risk to have taken but right now it's making me expect some tech-related content.

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

* OVerall nice practice with your prototype methods but [ahhhhhh](https://github.com/sschipke/gameTime/blob/master/src/FastMoney.js#L16) break this one out into some variables instead of nesting and chaining all on a single line.

* Lets add some methods to this [player class](https://github.com/sschipke/gameTime/blob/master/src/Player.js) ;) 

* Avoid storing duplicate information on multiple classes. e.g. it looks like both your Round class and Game class are storing a property called `answers` -- does this represent the same data in both classes? Are there subtle differences? Does it need to be stored on both classes or can you reference a single instance of one class and pass that information through to others that need it as an argument? The more data duplication you have, the harder it will be to keep things in sync as that data changes.


### Testing

* [ ] Novice - There is little or no evidence of testing in this application. ESLint shows 10+ complaints.
* [ ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.
* [ ] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.
* [x] Exceptional - Meets all requires of `Proficient`. In addition, the test suite makes use of mocks and stubs when appropriate. ESLint shows 0 complaints.

* I would maybe do a deep equal test on the actual array [here](https://github.com/sschipke/gameTime/blob/master/test/Game-test.js#L31-L34) rather than just asserting against the second player's name. Whenever it's possible to be more specific with our assertions, let's do that. There are some other tests I'd recommend the same thing, so take a look back at what's been written and see if there are any opportunities for more specificity in your assertions.

* Overall really nice test coverage and use of spies! Leverage those nested describe blocks for grouping tests that all exercise the same method (e.g. `submitGuess` tests for right vs. wrong answers)

### GitHub Collaboration/Workflow

* [ ] Novice - Developers do not tag instructors in the two required PRs by due dates listed in the project outline or tagged PR has fewer than 200 lines of code. The developer creating the PR does not summarize the changes or why the changes were made. Reviewers are not leaving line-by-line feedback/comments _or_ are merging the PR before changes are made.
* [ ] Advanced Beginner - Developers tag instructors in both required PRs by due dates _or_ in one of the two required. PR has less than the required lines of code in PR. Reviewers do not leave line-by-line feedback. May be merging PR before feedback is incorporated.
* [x] Proficient - Developers tag instructors in both required PRs by due dates. PR is over 100 lines of code. The developer creating the PR summarizes the changes made, why those changes were necessary, and asks for insights. Reviewers leave line-by-line comments/feedback and wait to merge PR until feedback is incorporated.
* [ ] Exceptional - Meets all expectations for `Proficient`. The feedback is both kind _and_ insightful. There may be numerous threads of conversation where developers go back and forth to find the best solution to the problems they are solving together.

- Nice code review! Love to see y'all getting into that work flow 
- PRs to us were nicely sized 
- Noah, it looks like your contributions were on the lower side of the groups (in terms of line numbers). It was still a good number of lines (~500), but I want to make sure that if you were driving and navigating, ensure that everyone gets an equal amount of driving time. That way, people's contributions truly match when they were there to work (co-authoring also doesn't fully share contributions)
- Most commits weren't too too long, make sure to always opt on the shorter side
- Most commit messages looked good, but don't forget to always capitalize them, and to keep them active / imperative

### Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.
* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 
* [x] Proficient - Everyone in the group has an opporunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.
* [ ] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.

- How did you end up solving communication struggles? Especially in terms of organization of tasks 
- Really good and thoughtful reflections from everyone,but make sure the talking points are streamlined. It's clear y'all learned a ton from the process and aseemed very excited to talk about it, but some times the points could runa little long. Just advice for future presntations,  but again, really great comments from everyone 
