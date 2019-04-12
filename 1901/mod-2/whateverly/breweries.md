# Whateverly 
* Students:
* Evaluator:

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

* Not entirely sure [this](https://github.com/saadricklamar/shakesbeer/blob/master/src/WelcomePage.js#L9-L14) needs to exist in state. Does it ever change? Maybe just in response to the props being passed down? If there are no methods that manipulate this piece of state, it's probably something that could go into a separate method that simply returns the results. e.g. in your render you would say something like:

```js
<Autocomplete usStates={this.getDataByState()} />
```

and in that `getDataByState` method, you would do your reduce and just return the results of that newly formatted dataset.

* Try to move away from the idea of your components representing a 'Page' -- React (and other client-side frameworks) are meant for building single-page applications where each component is simply a *piece* of the page, not an entirely independent page.

* The naming of this piece of [state](https://github.com/saadricklamar/shakesbeer/blob/master/src/Beer.js#L10) is a little off. It implies we're displaying/not displaying the Beer, when in reality it's just the description we're toggling. I'd rename this to something like `showDescription` instead.


* Good placement of your conditional logic [here](https://github.com/saadricklamar/shakesbeer/blob/master/src/Beer.js#L39-L45) (taking care of it in the parent component rather than in the BeerDescription component itself), but this would be a perfect use-case for that double && syntax:

```js
this.state.showDescription && <BeerDescription ...props />
```

so that you don't have to render 'null'







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

* [ x ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested.

* [ ] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features.

* [ ] Exceptional - Project has a running test suite that exercises the application used Enzyme. The test suite covers almost all aspects of the application.


Comments:

* Good test for the `getCities` method [here](https://github.com/saadricklamar/shakesbeer/blob/master/src/ResultsPage.test.js) but we're missing lots of other method tests in this file! Would like to see [this method](https://github.com/saadricklamar/shakesbeer/blob/master/src/App.js#L47-L50) get tested as well


* Careful of your it block descriptions [here](https://github.com/saadricklamar/shakesbeer/blob/master/src/Controls.test.js#L24-L36), we're not testing that we're simulating an event, we're testing what happens when that event is triggered. e.g. `it should invoke updateStyles when #styles is clicked`. I'd also be surprised if these tests are working the way you'd expect them to. You're manually invoking methods on your wrapper instance rather than simulating events.

* Lots of nice tiny, functional components that were kept simple and easy to test with snapshots but I think overall we're lacking in some of the method tests, especially around simulating events. I'd make this a big focus on your solo projects so that you can all get a bit more practice in with that, as you will be responsible for even more testing throughout Mod 3.


------------------------------------------------------------------

## Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.

* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 

* [ ] Proficient - Everyone in the group has an opportunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.

* [ ] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.


Comments:









