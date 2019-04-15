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

* Move [this type of conditional logic](https://github.com/MaxBSilver/marvel-whateverly/blob/master/src/components/card%20components/cardContainer/CardContainer.jsx#L12-L23) into the parent of CardContainer so that you don't bother booting up an entire component for no reason

* It's perfectly fine to write stateless components as classes (I actually prefer it), but if it doesn't have state, don't [set it up as an empty object](https://github.com/MaxBSilver/marvel-whateverly/blob/master/src/components/card%20components/cardContainer/CardContainer.jsx#L7-L8), just leave that whole piece out

* Better name for [this](https://github.com/MaxBSilver/marvel-whateverly/blob/master/src/components/card%20components/card/Card.jsx#L7) might be `displayInfo` -- calling it `toggleInfo` and setting it to true/false still doesn't really tell me if the information is displayed or not

* Ooooh, you never want to manually [manipulate](https://github.com/MaxBSilver/marvel-whateverly/blob/master/src/components/card%20components/card/Card.jsx#L18) something in your props. Props are intended to be immutable. Not sure what this is doing for you here, but I'd imagine you would just want to rely on that state change for `this.state.favorited` instead. e.g. in your default state in the constructor, instead of automatically setting `favorited` to `false`, I'd set it to whatever the prop equaled, then only rely on that state value afterwards:

```
this.state = {
  toggleInfo: false,
  favorited: props.card.favorited
}
```

* Instead of digging into [localStorage](https://github.com/MaxBSilver/marvel-whateverly/blob/master/src/components/card%20components/card/Card.jsx#L29) for the same value multiple times, this might be a good use-case for storing that data in state. Especially since you're manipulating it in `toggleFavorite`.

* Little bit too much going on [here](https://github.com/MaxBSilver/marvel-whateverly/blob/master/src/components/card%20components/card/Card.jsx#L37-L41) to use a ternary. Split this up a bit by pulling out the concat/includes methods and assigning that whole piece to a variable first.

* [This](https://github.com/MaxBSilver/marvel-whateverly/blob/master/src/components/card%20components/card/Card.jsx#L47-L70) is probably too much conditional JSX to throw into a ternary in your render method. If the code here is different enough, and the JSX represents something independent enough to warrant it's own variable name, I'd just create two separate functional components for these pieces. Otherwise I'd pick out just the lines that are different and create a couple different variables to represent those differing pieces to plug into the rest of the JSX.

* Little tricky to read the formatting of [these couple of lines](https://github.com/MaxBSilver/marvel-whateverly/blob/master/src/components/filter/Filter.jsx#L15-L18) you have a ternary split into 3 separate lines and then an if condition with no else/no curly braces on a single line. I'd refactor a bit here and give your code a little more room to breathe. It also looks like you want to set the state of movies to false no matter what based on that if condition....do you actually need that in a conditional? And does the ternary need its second half if you're just going to force movies to be false afterwards anyway?

* Getting a little gung-ho with [ternaries](https://github.com/MaxBSilver/marvel-whateverly/blob/master/src/components/filter/Filter.jsx#L48-L50). That's not a particularly bad use-case but you can simplify it even further:

```
let sortProperty = this.state.movies ? 'movies' : 'comics';
let valuesToSort = Object.values(this.state[sortProperty])
valuesToSort.sort(el1, el2 => { ...etc }
```

* Empty [strings](https://github.com/MaxBSilver/marvel-whateverly/blob/master/src/components/search/Search.jsx#L12) are already falsey in JavaScript.

* No need 2 abbr like [this](https://github.com/MaxBSilver/marvel-whateverly/blob/master/src/components/search/Search.jsx#L17) - just type out the whole thing it's not saving you any time by cutting out those characters.


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

* Remember [wrapper.state()](https://github.com/MaxBSilver/marvel-whateverly/blob/master/src/tests/Card.test.js#L41-L52) takes in an optional argument so you can test a single piece of state in isolation. e.g.

```js
wrapper.state('toggleInfo').toEqual(false);
```

* You also want to be testing that all those event handlers like these [onClick](https://github.com/MaxBSilver/marvel-whateverly/blob/master/src/components/card%20components/card/Card.jsx#L87-L91) have been simulated and are hooked up properly

* For your card container, you'd want to do some conditional snapshot testing (though as mentioned in the JS section above, you'd want to actually move that conditional logic up to the parent, which is also where you'd do the conditional snapshots in that case)

* Missing any/all event simulations for the filter and search tests









------------------------------------------------------------------

## Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.

* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 

* [ ] Proficient - Everyone in the group has an opportunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.

* [ ] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.


Comments:









