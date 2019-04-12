# Whateverly 
* Students: Kelly, Sally, Matt
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

* Lots of similar [code here](https://github.com/MatthewKaplan/yoga-fee-finder/blob/master/src/Studios/Studios.js#L10-L36) - could we clean up this conditional a little bit? At a quick glance, it looks like the only thing that's changing is the array that you're mapping over. Could you maybe do something like this instead:

```js
let yogaStudios = props.rendered.length ? props.rendered : props.studios;

yogaStudios.map(studio => {
  // render all your studioCards
});
```

* Not sure if you need to be preventing default behavior [on an input click](https://github.com/MatthewKaplan/yoga-fee-finder/blob/master/src/Controls/Controls.js#L10) in your methods here, as they're not wrapped in a form element. (Speaking of, for the sake of semantic HTML, you probably would want to change the section tag here into a form tag instead. ...in which case you would definitely need to prevent the default.)

* Looks like [this](https://github.com/MatthewKaplan/yoga-fee-finder/blob/master/src/App/App.js#L34-L39) could be simplified into a single if statement that runs your fetch call:

```js
if (nothingInStorage) {
  this.fetchData();
}

this.addImgs();
```

* I generally see this double-ampersand [syntax](https://github.com/MatthewKaplan/yoga-fee-finder/blob/master/src/App/App.js#L62-L71) in JSX for simple conditional rendering. You won't see it used like this for performaing any sort of conditional logic outside of that context. It's a little difficult to read/understand what's actually going to happen in this method, and I'm not 100% sure it behaves the same way. I'd stick to just using it in your JSX as you're rendering elements. For example, your conditional [rendering here](https://github.com/MatthewKaplan/yoga-fee-finder/blob/master/src/App/App.js#L113-L124) has two great use-cases for that && syntax rather than using ternaries ;) 

* Nice tiny [methods here](https://github.com/MatthewKaplan/yoga-fee-finder/blob/master/src/App/App.js#L81-L91)







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

* Small nitpick, but when you have [this much mock data](https://github.com/MatthewKaplan/yoga-fee-finder/blob/master/src/typeCard/TypeCard.test.js#L9-L71), I'd pull it out into a separate file to tuck it away a little bit and just import it with a single line.

* Overall good coverage on your snapshots and rendered output, though you have a couple tests like [this](https://github.com/MatthewKaplan/yoga-fee-finder/blob/master/src/Search/Search.test.js#L75-L78) and [this](https://github.com/MatthewKaplan/yoga-fee-finder/blob/master/src/typeCard/TypeCard.test.js#L106-L109) that aren't really doing anything for ya. You are already testing all of the rendered output with your snapshot tests, so finding a particular element and testing that it's there isn't going to give you much more assurance about your code.

* [Here](https://github.com/MatthewKaplan/yoga-fee-finder/blob/master/src/typeCard/TypeCard.test.js#L116) you are manually calling `setState` to change the typeId -- essentially *forcing* your test to pass. This means that the assertions here aren't really testing your application code, they're testing the manual setState you just called in your test file. You want to let your component do the work in order to update state. So you'd really want to be invoking your `setTypeId` method on your component and making sure the typeId has changed after that method gets called.

* You also want to be simulating events like [this](https://github.com/MatthewKaplan/yoga-fee-finder/blob/master/src/typeCard/TypeCard.js#L60) and [this](https://github.com/MatthewKaplan/yoga-fee-finder/blob/master/src/typeCard/TypeCard.js#L58) in your tests. 

* Little confused about the mock props you're passing in [here](https://github.com/MatthewKaplan/yoga-fee-finder/blob/master/src/Studios/Studios.test.js#L13) -- it looks like the component itself takes in `rendered` and `studios` as props (based on your render method [here](https://github.com/MatthewKaplan/yoga-fee-finder/blob/master/src/Studios/Studios.js#L10-L36)), but it doesn't seem like you're passing those in as your mock data in your test file for your snapshot.

* Running the simulations [here](https://github.com/MatthewKaplan/yoga-fee-finder/blob/master/src/Search/Search.test.js#L81) and [here](https://github.com/MatthewKaplan/yoga-fee-finder/blob/master/src/Controls/Controls.test.js#L57) but not actually making any expectations against it? It looks like overall you might be getting a bit lost on how to assert against what should happen after these simulations are made. I would recommend pairing up with another group and getting a little review on testing these user interactions so you can practice it thoroughly during your solo projects next week. [Good simulation here though!](https://github.com/MatthewKaplan/yoga-fee-finder/blob/master/src/Search/Search.test.js#L84-L87)





------------------------------------------------------------------

## Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.

* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 

* [ ] Proficient - Everyone in the group has an opportunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.

* [ ] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.


Comments:









