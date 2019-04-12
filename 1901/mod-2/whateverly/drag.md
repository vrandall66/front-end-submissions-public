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


* If all [this method](https://github.com/jacobogart/queenly/blob/master/src/components/Thumbnail.js#L8-L10) is doing is calling another one, you don't need it. You could just directly put `this.props.selectSearchResult` in your `onClick` attribute. Something like `onClick={() => this.props.selectSearchResult(params)}`

* Perfect use-case for a switch statement [here](https://github.com/jacobogart/queenly/blob/master/src/components/Sub_Info.js#L11-L22)!

* [Not sure what's happening here](https://github.com/jacobogart/queenly/blob/master/src/components/Sub_Info.js#L23-L31)? I've never seen an element attribute called `dangerouslySetInnerHTML` and it sounds...dangerous. It looks like maybe you're trying to fill that div with some HTML? In which case you should be able to do something like:

```js
let asset = this.generateImgTag(); 
// generateImgTag would be a method that returns the img tag populated with the appropriate attribute values

<div>
  {asset}
</div>
```

* Is [this](https://github.com/jacobogart/queenly/blob/master/src/components/SearchResults.js#L26-L28) doing anything/being used anywhere?


* Nice [destructuring here](https://github.com/jacobogart/queenly/blob/master/src/components/Queen_Main.js#L9-L13), I think there are quite a few other places you could implement this in other components!

* [This](https://github.com/jacobogart/queenly/blob/master/src/components/Hamburger.js#L11-L15) could be simplified to:

```js
  toggleBurger = () => {
    this.setState({ showMenu: !this.state.showMenu })
  };
```

* Unless these [icons](https://github.com/jacobogart/queenly/blob/master/src/components/Card.js#L15-L21) are changing in some way, they probably shouldn't be stored as state values. You could just create a plain old object literal to hold a mapping of which icon classes represent what type of icon and import that wherever you need it.



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

* Not totally sure what we've got going on in [this test](https://github.com/jacobogart/queenly/blob/master/src/tests/Thumbnail.test.js#L36-L40) -- there's a couple different expectations and they don't quite match the description of the it block. I would expect, based on the it block description and based on your component, that we would want to be simulating a click event here and asserting that our mock function, `selectSearchResult` was called. (Same thing with your SearchSuggestion component. Simulate the click event, don't manually invoke a method that isn't doing anything except calling another one). Overall it looks like there's some hesitation around simulating events in your test files...I'd recommend making that a focus for your solo projects so you can get some additional practice in with that flow.

* Would like to see a test for this [onClick function being called](https://github.com/jacobogart/queenly/blob/master/src/components/SearchResults.js#L34) 

* You'd also want to be doing some conditional snapshot tests to account for how the rendered output changes [here](https://github.com/jacobogart/queenly/blob/master/src/components/SearchResults.js#L12-L25) based on the length of your search results.  (e.g. shallow render one component with an array of elements, then another with an empty array, and make sure the rendered output matches what you'd expect in both scenarios)






------------------------------------------------------------------

## Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.

* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 

* [ ] Proficient - Everyone in the group has an opportunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.

* [ ] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.


Comments:









