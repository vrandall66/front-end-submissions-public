# Whateverly 
* Students:
* Evaluator:
* Repo: https://github.com/SallyHaefling/enpsychlopedia

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

* [ x ] Proficient - The application has many strong pages/interactions. The application can stand on its own to be used by instructor without guidance from a developer on the team.

* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, the application is fully responsive, and has clearly had special consideration around usability on devices. There no holes in functionality.


Comments:

* It can be hard to tell that you can scroll horizontally in each music category, I'd add some left/right arrows that denote you can move back and forth in that direction. 

* Any time a user can click on something, I would turn that cursor into a little hand with CSS (e.g. the photos for each band) - the drop shadow on hover is a nice touch and gives me some indication that it's clickable, but the cursor is the number 1 thing people look to change on clicakble elements. 

* Nice job getting an active state on those filtering buttons, but we lose it when we click into one of the bands. Would make sense for that to stick around as when I click out of the band, I'm still only seeing the filtered list in that category.

* Good job getting a modal window/popup implemented - those are hard! I like the semi-transparent background overlay as well. One extra reach for that would be to allow the user to click anywhere outside the popup in order to exit out of it, rather than having to click the x button in the top right corner. Popups are also a good place to implement some very subtle CSS transitions like fadein/fadeouts.









------------------------------------------------------------------

## CSS/Sass Style

* [ ] Novice - There are several (10+) instances of duplication and one or two major bugs. Developers write code with unnecessary selectors or tags which do not increase clarity.

* [ ] Advanced Beginner - There is some duplication (5-10 instances) in the codebase. There may be one to two minor bugs. There may be some unnecessary selectors or tags. Application adds organization for the whole stylesheet and within rules.

* [ x ] Proficient - Application is thoughtfully put together with comments to help guide organization. There may be some duplication (fewer than 5 instances) present. Comments are present to assist with organization of code.

* [ ] Exceptional - Meets all expectations for `Proficient`. The application has exceptionally well-factored CSS/Sass with all styles separated out into logical stylesheets. There are zero instances where an instructor would recommend taking a different approach.


Comments:

* Avoid naming color [variables](https://github.com/SallyHaefling/enpsychlopedia/blob/master/src/Styles/_SassMixins.scss#L5-L6) with their actual colors -- if you ever change the color scheme, you'll have to change the variable names now too rather than just the values. Make the names more generic for what those colors represent -- is it the primary color for call to action elements? the default text color? etc.

* Nice use of a mixin for your buttons, that's a good use-case for them. If this were a bigger app that required more CSS, I would break out your variables into a separate variables.scss file, and leave your mixins separate in mixins.scss. Because it's so tiny it's not that big of a deal, but that will be the organizational strategy you see elesewhere.









------------------------------------------------------------------

## JavaScript / React Style

* [ ] Novice - There is a significant amount of duplication and one or two major bugs. JavaScript does not follow the principles of `DRY` (Don't Repeat Yourself)

* [ ] Advanced Beginner - There is some duplication and there may be one or two major bugs. The application has large components and logic could be broken apart into smaller, stateless components. JavaScript may be hard to read/follow.

* [x] Proficient - Application has little to no duplication and no major bugs. Application has several components built out that logically break apart the functionality. JavaScript may be hard to follow at times but is generally easy to read/understand. 

* [ ] Exceptional - Application has exceptionally well-factored code with little or no duplication and all components separated out into logical components. There are zero instances where an instructor would recommend taking a different approach to design and component architecture. DRY and SRP (Single Responsibility Principle) practices are incorporated, making JavaScript very easy to follow/read.


Comments:


- Nice file structure! Organizing your components with related tests make it easy to work through the codebase.
- Nice, small methods on classes. Very digestable.
- Be careful with your heading levels. Several components across the app make use of the `h1` heading level. Remember that the use of heading levels should be used and implemented for the page as a whole, not just the component itself.
- Opportunities for refactoring what's rendered in `Popup` and `Genre`. There's a lot going on here - making it hard to read/follow


------------------------------------------------------------------

## GitHub Collaboration/Workflow

* [ ] Novice - Developers do not tag instructors in the two required PRs by due dates listed in the project outline or tagged PR has fewer than 200 lines of code. The developer creating the PR does not summarize the changes or why the changes were made. Reviewers are not leaving line-by-line feedback/comments _or_ are merging the PR before changes are made.

* [ ] Advanced Beginner - Developers tag instructors in both required PRs by due dates _or_ in one of the two required. PR has less than the required lines of code in PR. Reviewers do not leave line-by-line feedback. May be merging PR before feedback is incorporated.

* [ x ] Proficient - Developers tag instructors in both required PRs by due dates. PR is between 350 - 450 lines of code. The developer creating the PR summarizes the changes made, why those changes were necessary, and asks for insights. Reviewers leave line-by-line comments/feedback and wait to merge PR until feedback is incorporated.

* [ ] Exceptional - Meets all expectations for `Proficient`. The feedback is both kind _and_ insightful. There may be numerous threads of conversation where developers go back and forth to find the best solution to the problems they are solving together.


Comments:

Contribution breakdown:  
 _Mason: <x> 28 commits  4,904 ++  4,027 --_  
 _Sally: <x> 45 commits  21,726 ++  4,103 --_  
 _David: <x> 31 commits  10,000 ++  7,685 --_  

* Overall as a group you probably need a bit more commits -- 77 likely means that each commit is doing too much work and includes more changesets than a single piece of functionality or work. I'd always aim to be well over 100 commits on projects of this size, especially when a lot of your commits are repeats like 'Update README'






------------------------------------------------------------------

## Testing

* [ ] Novice - There is little or no evidence of testing in the application.

* [ ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested.

* [ x ] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features.

* [ ] Exceptional - Project has a running test suite that exercises the application used Enzyme. The test suite covers almost all aspects of the application.


Comments:

* Controls test is missing simulations for all the click events for `getActivity`

* Genre test is missing assertion for state changes made in getActivity






------------------------------------------------------------------

## Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.

* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 

* [X] Proficient - Everyone in the group has an opportunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.

* [ ] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.


Comments:

* Good enthusiasm (David)
* The gifs are great to show your app
* When code was show, the snippets were small, which is great






