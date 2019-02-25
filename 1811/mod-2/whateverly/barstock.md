# Whateverly 
* Students:
* Evaluator:
* Repo: https://github.com/TomWilhoit/BarStock

# Rubric

## Specification Adherence

* [ ] Novice - README is missing or incomplete. Codebase is not organized. User stories from group are never submitted. Application does not solve the presented problem.

* [ ] Advanced Beginner - README is complete. Codebase is organized. User stories are completed; however, may be late. Some user stories may be unclear or hard to understand. Application is close to solving presented problem.

* [X] Proficient - Developers turn in user stories on time and iterate on user stories throughout the life of the project, as needed. User stories have enough detail - such that an outside developer could jump right in and help with user stories/tickets. Application solves the presented problem.

* [ ] Exceptional - Meets all expectations for `Proficient`. Developers may use personas to help guide their user stories. Developers may also incorporate other tools to assist in planning - workflow diagrams, story maps, etc.



------------------------------------------------------------------

## UI/UX

* [ ] Novice - The application is confusing or difficult to use. The final project presents an interface that is incomplete.

* [ ] Advanced Beginner - The application may be confusing or difficult to use at times. The application shows effort in the interface, but the result is not effective because UX and/or UI still present an application that is incomplete or difficult to use. It is not clear that the user stories helped to guide UX.

* [ ] Proficient - The application has many strong pages/interactions. The application can stand on its own to be used by instructor without guidance from a developer on the team.

* [ x ] Exceptional - Meets all expectations for `Proficient`. In addition, the application is fully responsive, and has clearly had special consideration around usability on devices. There no holes in functionality.


Comments:

* This looks great! Incredibly clean and simple. Responsiveness is really effective at multiple breakpoints. Good hierarchy of font styling that clearly denotes what's most/least important on the page at the time. Nice display of 'context' - where I only see what I need to see at any given time. 

* I would make it a bit more obvious that I can click on the subcategories under beer/liquor to expand and collapse them. Maybe just an up/down or plus/minus icon would be enough to suffice. 

* Even though we're mobile-first which doesn't generally have a concept of 'hover' effects, it would still be nice to have those for desktop on clickable elements. (The only one I really notice is the beer/liquor hovers.) 

* Rather than a login button, I'd ask some sort of other question like 'Name of Your Bar' -- I'd be concerned with potential employers recognizing that the login/authentication isn't actually a secure login and not knowing if you recognize that or not. You would never store authentication credentials in state the way you are, so this is something I'd consider taking out or changing to something else.








------------------------------------------------------------------

## CSS/Sass Style

* [ ] Novice - There are several (10+) instances of duplication and one or two major bugs. Developers write code with unnecessary selectors or tags which do not increase clarity.

* [ ] Advanced Beginner - There is some duplication (5-10 instances) in the codebase. There may be one to two minor bugs. There may be some unnecessary selectors or tags. Application adds organization for the whole stylesheet and within rules.

* [ x ] Proficient - Application is thoughtfully put together with comments to help guide organization. There may be some duplication (fewer than 5 instances) present. Comments are present to assist with organization of code.

* [ ] Exceptional - Meets all expectations for `Proficient`. The application has exceptionally well-factored CSS/Sass with all styles separated out into logical stylesheets. There are zero instances where an instructor would recommend taking a different approach.


Comments:

* If you're going to have a CSS directory and an images directory, make sure your files are in the right place. There are a lot of images in the [/css](https://github.com/TomWilhoit/BarStock/tree/master/src/css) directory that should probably be moved out.

* Rather than naming your color variables [by what color they are, like blue](https://github.com/TomWilhoit/BarStock/blob/master/src/css/App.scss#L4-L10) name them by what that color represents in your design. Is it a call-to-action color for buttons? Is it a bold-text-color? Is it a color for emphasized-text? The problem with naming your colors based on what color they actually are is that if you ever do a redesign and change your color scheme, you have to change all your variable names as well. Otherwise, nice usage of variables, though you'd want to pull them out into their own file like `variables.scss` so that they all live in one place and you only ever have to update them in that single file.

* I'd cut back just slightly on the amount of nesting you're doing -- for example, I doubt this [login-quote](https://github.com/TomWilhoit/BarStock/blob/master/src/css/Login.scss#L29-L34) styling actually *needs* to be nested under the .Login selector. If you don't have any elements with a class of login-quote *outside* of the element with a class of Login, you shouldn't have to nest it in your Sass. Unecessary nesting causes the compiled css to be overly specific and more bloated than it should be.








------------------------------------------------------------------

## JavaScript / React Style

* [ ] Novice - There is a significant amount of duplication and one or two major bugs. JavaScript does not follow the principles of `DRY` (Don't Repeat Yourself)

* [ ] Advanced Beginner - There is some duplication and there may be one or two major bugs. The application has large components and logic could be broken apart into smaller, stateless components. JavaScript may be hard to read/follow.

* [x] Proficient - Application has little to no duplication and no major bugs. Application has several components built out that logically break apart the functionality. JavaScript may be hard to follow at times but is generally easy to read/understand. 

* [ ] Exceptional - Application has exceptionally well-factored code with little or no duplication and all components separated out into logical components. There are zero instances where an instructor would recommend taking a different approach to design and component architecture. DRY and SRP (Single Responsibility Principle) practices are incorporated, making JavaScript very easy to follow/read.

Comments:

- Nice job with breaking out components for Header and Footer
- A little more organization in your [file structure](https://reactjs.org/docs/faq-structure.html) would make the codebase easier to work through. You could place the components all into their own folder and move any assets into their own folder (similar to how you have your stylesheets in their own directory)
- Opportunities for refactoring methods and renders within the components. The size of the components and renders make the code difficult to follow/read. 


------------------------------------------------------------------

## GitHub Collaboration/Workflow

* [ ] Novice - Developers do not tag instructors in the two required PRs by due dates listed in the project outline or tagged PR has fewer than 200 lines of code. The developer creating the PR does not summarize the changes or why the changes were made. Reviewers are not leaving line-by-line feedback/comments _or_ are merging the PR before changes are made.

* [ ] Advanced Beginner - Developers tag instructors in both required PRs by due dates _or_ in one of the two required. PR has less than the required lines of code in PR. Reviewers do not leave line-by-line feedback. May be merging PR before feedback is incorporated.

* [ x ] Proficient - Developers tag instructors in both required PRs by due dates. PR is between 350 - 450 lines of code. The developer creating the PR summarizes the changes made, why those changes were necessary, and asks for insights. Reviewers leave line-by-line comments/feedback and wait to merge PR until feedback is incorporated.

* [ ] Exceptional - Meets all expectations for `Proficient`. The feedback is both kind _and_ insightful. There may be numerous threads of conversation where developers go back and forth to find the best solution to the problems they are solving together.


Comments:

Contribution breakdown:  
 _Taylor: <x> 32 commits  2,851 ++  1,257 --_  
 _Tom: <x> 16 commits  22,679 ++  4,997 --_  
 _Mike: <x> 16 commits  2,928 ++  1,185 --_  

* Look into git squashing for getting rid of things like all of [these](https://github.com/TomWilhoit/BarStock/commits/master) update readme commits.






------------------------------------------------------------------

## Testing

* [ ] Novice - There is little or no evidence of testing in the application.

* [ ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested.

* [ ] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features.

* [ ] Exceptional - Project has a running test suite that exercises the application used Enzyme. The test suite covers almost all aspects of the application.


Comments:










------------------------------------------------------------------

## Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.

* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 

* [X] Proficient - Everyone in the group has an opportunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.

* [ ] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.


Comments:

* Intro was great - the background was a bit long, wanted to get to the point of the problem being solved a little sooner - keep in mind people in the audience who are not familiar with owning a bar
* Some gifs were a bit small on the screen - hard to see the functionality you were trying to show. Try to make gifs as close to fullscreen as you can
* When showing code, keep is as small as possible with snippets
* Great to hear about TDD lesson learned and also that datasets are never perfect







