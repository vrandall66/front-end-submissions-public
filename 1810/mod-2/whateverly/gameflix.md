# Whateverly 
* Students: Justin Duncan, Matthew Foxwell, and Whitney Burton
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

* [x] Advanced Beginner - There is some duplication and there may be one or two major bugs. The application has large components and logic could be broken apart into smaller, stateless components. JavaScript may be hard to read/follow.

* [ ] Proficient - Application has little to no duplication and no major bugs. Application has several components built out that logically break apart the functionality. JavaScript may be hard to follow at times but is generally easy to read/understand. 

* [ ] Exceptional - Application has exceptionally well-factored code with little or no duplication and all components separated out into logical components. There are zero instances where an instructor would recommend taking a different approach to design and component architecture. DRY and SRP (Single Responsibility Principle) practices are incorporated, making JavaScript very easy to follow/read.


Comments:

* React helps you build these "single-page" applications, so you shouldn't be naming your components like 'SearchPage.js' -- the content that the Search component provides you doesn't represent an entire page - it represents a single component on a page. It wouldn't make sense to view this component on it's own, with nothing else on the page.

* Nice use of [destructuring](https://github.com/whitneyburton/gameflix/blob/master/src/Components/SearchPage.js#L7)

* Lots of [divs all over the place](https://github.com/whitneyburton/gameflix/blob/master/src/Components/SearchPage.js#L10-L12) -- whenever you have a list of something, you should try to use an ol/ul and li tags instead to be a bit more semantic.

* You could do [this](https://github.com/whitneyburton/gameflix/blob/master/src/Components/PopUp.js#L6-L9) classname assignment on one line:

```
let className = isSearch ? "search-popup" : "PopUp"
```

That's a little more readable and a more common convention for working with ternaries. Though I'd also stay away from using the word `className` -- React needs that for setting classes on elements in JSX and you might run into naming collisions if you're using that word as a variable name as well.

* You shouldn't be doing any [document query selectors](https://github.com/whitneyburton/gameflix/blob/master/src/Components/Navbar.js#L7) in a React app -- this would be equivalent to combining React and jQuery. If you need to toggle a class, you should be conditionally setting it on the element that requires it based on some value in state/props. e.g.

```
<li className={stateValue ? 'yes-class' : 'no-class' }>lorem ipsum</li>
```

* Same thing [here](https://github.com/whitneyburton/gameflix/blob/master/src/Components/App.js#L85-L89) -- set the value attributes of those inputs to a value in state that automatically updates/clears out based on that state value so you don't have to do a DOM lookup for it.

* This [string](https://github.com/whitneyburton/gameflix/blob/master/src/Components/App.js#L98) is hard to read because it's not in camelCase. Make sure you're camelCasing your variables and values. e.g. `resetAll`

* Overall, your app component is reallyyyyy big and holding onto way too much state that's probably not necessary. You should find some ways to break these things out into smaller components that manage their own state. 

* We don't want to incorporate [state](https://github.com/whitneyburton/gameflix/blob/master/src/Components/App.js#L234-L238) just to determine which components should be rendered. This should be determined instead by user interactions (e.g. if I've searched for a game, I should see a game card, if I havent, the search state should be empty. If the search state is empty, I should see the landing page) 

* Is this really a [nav](https://github.com/whitneyburton/gameflix/blob/master/src/Components/Featured.js#L7)?

* Rather than relying on DOM elements [here](https://github.com/whitneyburton/gameflix/blob/master/src/Components/Carousel.js#L8-L12) and accessing their parent elements, you should have some values in state that determine the positioning of the carousel so you can apply CSS attributes to the elements that will position the carousel correctly. When you're working in React, you want to avoid doing any sort of manual DOM traversal to find or select elements -- it takes away from the magic of React.












------------------------------------------------------------------

## GitHub Collaboration/Workflow


* [ ] Novice - Developers do not tag instructors in the two required PRs by due dates listed in the project outline or tagged PR has fewer than 200 lines of code. The developer creating the PR does not summarize the changes or why the changes were made. Reviewers are not leaving line-by-line feedback/comments _or_ are merging the PR before changes are made.

* [ ] Advanced Beginner - Developers tag instructors in both required PRs by due dates _or_ in one of the two required. PR has less than the required lines of code in PR. Reviewers do not leave line-by-line feedback. May be merging PR before feedback is incorporated.

* [x] Proficient - Developers tag instructors in both required PRs by due dates. PR is between 350 - 450 lines of code. The developer creating the PR summarizes the changes made, why those changes were necessary, and asks for insights. Reviewers leave line-by-line comments/feedback and wait to merge PR until feedback is incorporated.

* [ ] Exceptional - Meets all expectations for `Proficient`. The feedback is both kind _and_ insightful. There may be numerous threads of conversation where developers go back and forth to find the best solution to the problems they are solving together.

Comments:

Contribution breakdown:  
Justin: 37 commits  
Whitney: 45 commits  
Matt: 25 commits  

- Good amount of conversation and useful comments happening in PRs! Good line-by-line feedback.
- Tagged instructors 12/21, and 12/27. Each PR was less than 200 lines of code to review.

------------------------------------------------------------------

## Testing

* [x] Novice - There is little or no evidence of testing in the application.

* [ ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested.

* [ ] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features.

* [ ] Exceptional - Project has a running test suite that exercises the application used Enzyme. The test suite covers almost all aspects of the application.


Comments:

* Per the history, looks like Justin did the majority of the testing with additions from Whitney. No contributions were found by Matt. It is important that all group members make sure that everyone on the project has the opportunity to test.
* Lots of missing tests - there are no tests for `NavBar`, inconsistent snapshot testing and testing for clickHandlers across components, missing tests in `Carousel`, and state and methods are _not_ tested for anything in `App`. Per the history of commits, it looks like tests were written right after the testing lesson and not picked up again until 1-2 day before the project due date. For future projects, be sure to write tests early and try to finish the majority of your testing well before the project due date!


------------------------------------------------------------------

## Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.

* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 

* [x] Proficient - Everyone in the group has an opporunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.

* [ ] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.

Comments:

- Pay attention to your body language and where your eyes are focused when you are presenting - avoid looking at the floor
- Many of the slides aren't adding much to the presentation - code snippets or other visuals would strengthen the presentation
- Nice comic relief regarding the monster method in your application
- Would like to see the demo of the app a bit sooner - was a bit delayed
- Nice job using a recording for the application
- Good positivity/smiles during the presentation
- Don't throw in F bombs or curse words - always a bit risky in a formal presentation
- Love your showcasing of the mobile design as part of your project