# Whateverly 
* Students: Gabriel Inzurriaga, Shannon Moranetz, and Paul Vangelakos
* Evaluator: Brittany, Pam, and Robbie

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

* [ ] Advanced Beginner - There is some duplication (5-10 instances) in the codebase. There may be one to two minor bugs. There may be some unncessary selectors or tags. Application adds organization for the whole stylesheet and within rules.

* [ ] Proficient - Application is thoughtfully put together with comments to help guide organization. There may be some duplication (fewer than 5 instances) present. Comments are present to assist with organization of code.

* [ ] Exceptional - Meets all expectations for `Proficient`. The application has exceptionally well-factored CSS/Sass with all styles separated out into logical stylesheets. There are zero instances where an instructor would recommend taking a different approach.


Comments:










------------------------------------------------------------------

## JavaScript / React Style

* [ ] Novice - There is a significant amount of duplication and one or two major bugs. JavaScript does not follow the principles of `DRY` (Don't Repeat Yourself)

* [ ] Advanced Beginner - There is some duplication and there may be one or two major bugs. The application has large components and logic could be broken apart into smaller, stateless components. JavaScript may be hard to read/follow.

* [x] Proficient - Application has little to no duplication and no major bugs. Application has several components built out that logically break apart the functionality. JavaScript may be hard to follow at times but is generally easy to read/understand. 

* [ ] Exceptional - Application has exceptionally well-factored code with little or no duplication and all components separated out into logical components. There are zero instances where an instructor would recommend taking a different approach to design and component architecture. DRY and SRP (Single Responsibility Principle) practices are incorporated, making JavaScript very easy to follow/read.


Comments:

* Really nice, tiny methods! Great job breaking your code out into different methods to keep them easily testable and readable

* [This](https://github.com/shannonmoranetz/mentalitea/blob/master/src/TeaCard.js#L12) method could be named better -- you don't have to include the word 'function', we know it's a function because of the way it's written and the way it's referenced with parens. Also, `toggleExpand` tells me something that's going to happen with the UI - but not what it means. What does it mean when a TeaCard is expanding? Is it showing more information about that tea? If so, I'd name it something like `toggleTeaDetails` to denote that it is showing or hiding content, not just 'expanding'.

* Little confused by the class names [here](https://github.com/shannonmoranetz/mentalitea/blob/master/src/TeaCard.js#L19-L25) -- it looks like this condition is saying if the card *is* expanded, but then the classnames all say `unexpanded`, and vice-versa in the else statement.

* The conditional logic [here](https://github.com/shannonmoranetz/mentalitea/blob/master/src/TeaCard.js#L18-L56) isn't terribly unreadable, but you could clean it up a bit by making another component. Maybe you have a `TeaPreview` component that just displays the name and image, and a `TeaDetails` component that displays all the information about that tea. Then you can just do an if/else for which component to render, rather than returning two separate chunks of JSX.

* You will learn about this more in Mod 3, but if you're looking for some additional things to look into ahead of time, you might want to do some research on Promise.all() for doing multiple fetch requests like you're doing [here](https://github.com/shannonmoranetz/mentalitea/blob/master/src/App.js#L23-L39)

* [This](https://github.com/shannonmoranetz/mentalitea/blob/master/src/Splash.js#L33-L36) looks like a good use-case for an ordered list rather than paragraph tags ;)

* Nice prototype iteration for generating your [options here](https://github.com/shannonmoranetz/mentalitea/blob/master/src/Splash.js#L41-L46)

* Rather than having additional state that determines if a component renders or not, like [this](https://github.com/shannonmoranetz/mentalitea/blob/master/src/App.js#L13), I would leverage whatever information actually determines if that component is shown. To me, it looks like you will only show the splash page if there is no mood selected. I would use that piece of state, `userSelectedMood`, to say "If there is no selected mood, render the splash component, otherwise render the controls component"







------------------------------------------------------------------

## GitHub Collaboration/Workflow

* [ ] Novice - Developers do not tag instructors in the two required PRs by due dates listed in the project outline or tagged PR has fewer than 200 lines of code. The developer creating the PR does not summarize the changes or why the changes were made. Reviewers are not leaving line-by-line feedback/comments _or_ are merging the PR before changes are made.

* [ ] Advanced Beginner - Developers tag instructors in both required PRs by due dates _or_ in one of the two required. PR has less than the required lines of code in PR. Reviewers do not leave line-by-line feedback. May be merging PR before feedback is incorporated.

* [ ] Proficient - Developers tag instructors in both required PRs by due dates. PR is between 350 - 450 lines of code. The developer creating the PR summarizes the changes made, why those changes were necessary, and asks for insights. Reviewers leave line-by-line comments/feedback and wait to merge PR until feedback is incorporated.

* [ ] Exceptional - Meets all expectations for `Proficient`. The feedback is both kind _and_ insightful. There may be numerous threads of conversation where developers go back and forth to find the best solution to the problems they are solving together.


Comments:










------------------------------------------------------------------

## Testing

* [ ] Novice - There is little or no evidence of testing in the application.

* [ ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The applicaiton contains numberous holes in testing and/or many features are untested.

* [ ] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features.

* [ ] Exceptional - Project has a running test suite that exercises the application used Enzyme. The test suite covers almost all aspects of the application.


Comments:










------------------------------------------------------------------

## Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.

* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 

* [ ] Proficient - Everyone in the group has an opporunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.

* [ ] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.


Comments:









