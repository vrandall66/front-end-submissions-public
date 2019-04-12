# Whateverly 
* Students:
* Evaluator: Pam, Robbie, Brittany

# Rubric

## Specification Adherence

* [ ] Novice - README is missing or incomplete. Codebase is not organized. User stories from group are never submitted. Application does not solve the presented problem.

* [ ] Advanced Beginner - README is complete. Codebase is organized. User stories are completed; however, may be late. Some user stories may be unclear or hard to understand. Application is close to solving presented problem.

* [ ] Proficient - Developers turn in user stories on time and iterate on user stories throughout the life of the project, as needed. User stories have enough detail - such that an outside developer could jump right in and help with user stories/tickets. Application solves the presented problem.

* [ ] Exceptional - Meets all expectations for `Proficient`. Developers may use personas to help guide their user stories. Developers may also incorporate other tools to assist in planning - workflow diagrams, story maps, etc.


Comments:










------------------------------------------------------------------

## UI/UX

* [ ] Novice - The application is confusing or difficult to use. The final project presents an interface that is incomplete.

* [ ] Advanced Beginner - The application may be confusing or difficult to use at times. The application shows effort in the interface, but the result is not effective because UX and/or UI still present an application that is incomplete or difficult to use. It is not clear that the user stories helped to guide UX.

* [ ] Proficient - The application has many strong pages/interactions. The application can stand on its own to be used by instructor without guidance from a developer on the team.

* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, the application is fully responsive, and has clearly had special consideration around usability on devices. There no holes in functionality.


Comments:










------------------------------------------------------------------

## CSS/Sass Style

* [ ] Novice - There are several (10+) instances of duplication and one or two major bugs. Developers write code with unnecessary selectors or tags which do not increase clarity.

* [ ] Advanced Beginner - There is some duplication (5-10 instances) in the codebase. There may be one to two minor bugs. There may be some unnecessary selectors or tags. Application adds organization for the whole stylesheet and within rules.

* [ ] Proficient - Application is thoughtfully put together with comments to help guide organization. There may be some duplication (fewer than 5 instances) present. Comments are present to assist with organization of code.

* [ ] Exceptional - Meets all expectations for `Proficient`. The application has exceptionally well-factored CSS/Sass with all styles separated out into logical stylesheets. There are zero instances where an instructor would recommend taking a different approach.


Comments:










------------------------------------------------------------------

## JavaScript / React Style

* [ ] Novice - There is a significant amount of duplication and one or two major bugs. JavaScript does not follow the principles of `DRY` (Don't Repeat Yourself)

* [ ] Advanced Beginner - There is some duplication and there may be one or two major bugs. The application has large components and logic could be broken apart into smaller, stateless components. JavaScript may be hard to read/follow.

* [ x ] Proficient - Application has little to no duplication and no major bugs. Application has several components built out that logically break apart the functionality. JavaScript may be hard to follow at times but is generally easy to read/understand. 

* [ ] Exceptional - Application has exceptionally well-factored code with little or no duplication and all components separated out into logical components. There are zero instances where an instructor would recommend taking a different approach to design and component architecture. DRY and SRP (Single Responsibility Principle) practices are incorporated, making JavaScript very easy to follow/read.


Comments:

* Nice [destructuring](https://github.com/jarrettkong/climb-on/blob/master/src/components/Place.jsx#L10)

* You can always just check the length instead of [length > 0](https://github.com/jarrettkong/climb-on/blob/master/src/components/Place.jsx#L12) - 0 is a falsey value in JavaScript

* Don't rely just on the [index](https://github.com/jarrettkong/climb-on/blob/master/src/components/Places.jsx#L19) as your unique key -- you will run into problems as your dataset potentially changes. It's best to rely on some sort of unique ID or other identifier, and at the very least, prefix that index with something like `place-${index}`

* You could probably create an array of these [difficulty levels](https://github.com/jarrettkong/climb-on/blob/master/src/components/SideBar.jsx#L75-L124) and map over it to generate all of these divs -- I'd break it out into a separate method like `generateDifficultyFilters` that returns the generated JSX so you can kind of tuck it away and DRY up your code. Same thing with your type filters if you want, though since there's only 3 of those it won't save you quite as much.

* Some duplicate state in the [App](https://github.com/jarrettkong/climb-on/blob/master/src/App.jsx#L13-L17) and [SideBar](https://github.com/jarrettkong/climb-on/blob/master/src/components/SideBar.jsx) component. This information should live in a single place (I'd imagine it would need to exist in the App component as it seems important for some siblings to know about it).

* Nice job working with [Promise.all()](https://github.com/jarrettkong/climb-on/blob/master/src/App.jsx#L29-L34)






------------------------------------------------------------------

## GitHub Collaboration/Workflow

* [ ] Novice - Developers do not tag instructors in the two required PRs by due dates listed in the project outline or tagged PR has fewer than 200 lines of code. The developer creating the PR does not summarize the changes or why the changes were made. Reviewers are not leaving line-by-line feedback/comments _or_ are merging the PR before changes are made.

* [ ] Advanced Beginner - Developers tag instructors in both required PRs by due dates _or_ in one of the two required. PR has less than the required lines of code in PR. Reviewers do not leave line-by-line feedback. May be merging PR before feedback is incorporated.

* [ ] Proficient - Developers tag instructors in both required PRs by due dates. PR is between 350 - 450 lines of code. The developer creating the PR summarizes the changes made, why those changes were necessary, and asks for insights. Reviewers leave line-by-line comments/feedback and wait to merge PR until feedback is incorporated.

* [ ] Exceptional - Meets all expectations for `Proficient`. The feedback is both kind _and_ insightful. There may be numerous threads of conversation where developers go back and forth to find the best solution to the problems they are solving together.


Comments:

Contribution breakdown:  
 _student1: <x> commits_  
 _student2: <x> commits_  
 _student3: <x> commits_  








------------------------------------------------------------------

## Testing

* [ ] Novice - There is little or no evidence of testing in the application.

* [ ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested.

* [ ] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features.

* [ x ] Exceptional - Project has a running test suite that exercises the application used Enzyme. The test suite covers almost all aspects of the application.


Comments:

* Good [conditional snapshotting here](https://github.com/jarrettkong/climb-on/blob/master/src/tests/Place.test.js)

* Really nice testing of simulated events across the board, your methods are nice and tiny which hopefully made this much easier. Good method coverage on even the more complex components like SideBar.

* Nitpick You won't see [snake_case](https://github.com/jarrettkong/climb-on/blob/master/src/tests/Sidebar.test.js#L8) a ton in the JS ecosystem. We're mostly into the camelCase these days, but either way just be consistent.

* I think your it block descriptions [here](https://github.com/jarrettkong/climb-on/blob/master/src/tests/App.test.js#L166-L170) might be a little off? Your testing opposite behavior but have the same description.

------------------------------------------------------------------

## Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.

* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 

* [ ] Proficient - Everyone in the group has an opportunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.

* [ ] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.


Comments:









