# Whateverly 
* Students: Heather Hartley, Eric Weissman, and Tom Wilhoit
* Evaluator: Brittany, Pam, and Robbie

# Rubric

## Specification Adherence

* [ ] Novice - README is missing or incomplete. Codebase is not organized. User stories from group are never submitted. Application does not solve the presented problem.

* [ ] Advanced Beginner - README is complete. Codebase is organized. User stories are completed; however, may be late. Some user stories may be unclear or hard to understand. Application is close to solving presented problem.

* [x] Proficient - Developers turn in user stories on time and iterate on user stories throughout the life of the project, as needed. User stories have enough detail - such that an outside developer could jump right in and help with user stories/tickets. Application solves the presented problem.

* [ ] Exceptional - Meets all expectations for `Proficient`. Developers may use personas to help guide their user stories. Developers may also incorporate other tools to assist in planning - workflow diagrams, story maps, etc.


Comments:

* Put the screenshots before the wireframes in the README. An employer wants to see what the app looks like, and then maybe they'll be curious about your process. The wireframes looks good.
* There are too many screenshots/gifs, especially since they all kind of look the same - I'm not sure what to look for in each gif. You could do with one or two gifs.
* In the future, break out your user stories into multiple issues so each issue can be tackled independently.

------------------------------------------------------------------

## UI/UX

* [ ] Novice - The application is confusing or difficult to use. The final project presents an interface that is incomplete.

* [ ] Advanced Beginner - The application may be confusing or difficult to use at times. The application shows effort in the interface, but the result is not effective because UX and/or UI still present an application that is incomplete or difficult to use. It is not clear that the user stories helped to guide UX.

* [x] Proficient - The application has many strong pages/interactions. The application can stand on its own to be used by instructor without guidance from a developer on the team.

* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, the application is fully responsive, and has clearly had special consideration around usability on devices. There no holes in functionality.


Comments:

* The font choice is nice for the topic as well as the color scheme.
* The ice cream cone images looks a little squished (maybe it just needs some room on the bottom/top of the image) as well as the individual ice cream flavor images.
* The pints for each ice cream are nice - they are a little big for the space used, especially since there are so many flavors.
* The ice cream show pages (popups) are a little plain - could use the space a little more effectively. There is some unused space. 



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

* [x] Proficient - Application has little to no duplication and no major bugs. Application has several components built out that logically break apart the functionality. JavaScript may be hard to follow at times but is generally easy to read/understand. 

* [ ] Exceptional - Application has exceptionally well-factored code with little or no duplication and all components separated out into logical components. There are zero instances where an instructor would recommend taking a different approach to design and component architecture. DRY and SRP (Single Responsibility Principle) practices are incorporated, making JavaScript very easy to follow/read.


Comments:

* You could destructure all of your props [here](https://github.com/ericweissman/icecream_whateverly/blob/master/src/SearchByParlor.js#L5) (and in all of your components!) instead of just the one by doing something like:

```
let { parlors, searchParlor } = props;
```

* HTML structure is a bit weird [here](https://github.com/ericweissman/icecream_whateverly/blob/master/src/ParlorDetail.js#L11-L22) - you have an li tag, with a div inside it, with another li tag inside of it? I would rip out that div and inner li and replace it with a span, if that's even necessary. You could just return a string here to fill in the inner text of the top level li.

* You will learn about this more in Mod 3, but if you're looking for some additional things to look into ahead of time, you might want to do some research on Promise.all() for doing multiple fetch requests like you're doing [here](https://github.com/ericweissman/icecream_whateverly/blob/master/src/App.js#L20-L41)

* Nice clean [render](https://github.com/ericweissman/icecream_whateverly/blob/master/src/App.js#L51-L68) method by splitting out your JSX into many components, good job.

* Little vague [here](https://github.com/ericweissman/icecream_whateverly/blob/master/src/ParlorCard.js#L10), what about details? Show them? Hide them? And [here](https://github.com/ericweissman/icecream_whateverly/blob/master/src/App.js#L14)  - value for what?

* I don't love seeing two [return statements](https://github.com/ericweissman/icecream_whateverly/blob/master/src/CardContainer.js#L19-L22) like this --- my eye immediately goes to the second one, where you're returning an empty array, and it makes me wonder what the rest of the function is doing all that work for. I would refactor to something like:

```
let parlorFlavors = [];

if (foundParlor) {
  parlorFlavors = foundParlor.flavors;
}

return parlorFlavors
```

This way, you're always returning the same variable -- parlorFlavors -- but what it represents is just reassigned if your condition is true.



------------------------------------------------------------------

## GitHub Collaboration/Workflow

* [ ] Novice - Developers do not tag instructors in the two required PRs by due dates listed in the project outline or tagged PR has fewer than 200 lines of code. The developer creating the PR does not summarize the changes or why the changes were made. Reviewers are not leaving line-by-line feedback/comments _or_ are merging the PR before changes are made.

* [x] Advanced Beginner - Developers tag instructors in both required PRs by due dates _or_ in one of the two required. PR has less than the required lines of code in PR. Reviewers do not leave line-by-line feedback. May be merging PR before feedback is incorporated.

* [x] Proficient - Developers tag instructors in both required PRs by due dates. PR is between 350 - 450 lines of code. The developer creating the PR summarizes the changes made, why those changes were necessary, and asks for insights. Reviewers leave line-by-line comments/feedback and wait to merge PR until feedback is incorporated.

* [ ] Exceptional - Meets all expectations for `Proficient`. The feedback is both kind _and_ insightful. There may be numerous threads of conversation where developers go back and forth to find the best solution to the problems they are solving together.


Comments:

Contribution breakdown:
Eric: 37 commits  
Tom: 12 commits  
Heather: 56 commits  

- Looking at contributions in a group of three (from commits as well as actual code/features added) the split of the work does not seem balanced.
- Would like to see more back/forth conversation in your PRs. This [PR](https://github.com/ericweissman/icecream_whateverly/pull/59) and [this](https://github.com/ericweissman/icecream_whateverly/pull/67) are good examples of where some of this happens; however, conversation is inconsistent or completely lacking in other PRs. Lots of instances of a PR creator asking for feedback and not receiving a response.
- Tagged instructors 12/21 and 1/2 (2 days past Day 8). One PR was about 400 lines, other was around 200.










------------------------------------------------------------------

## Testing

* [ ] Novice - There is little or no evidence of testing in the application.

* [x] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested.

* [x] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features.

* [ ] Exceptional - Project has a running test suite that exercises the application used Enzyme. The test suite covers almost all aspects of the application.


Comments:


* Nice job with tests directory - the organization makes it much easier to go through the testing suite while comparing tests to the implemented code
* Additional assertions could be added to make sure that mock functions are being called a set number of times when a method is invoked.
should change ParlorCard details state to true when the getParlorDetails method is called - what does this mean in terms of the user
* When you are testing for updates to state, you'll typically want to check for the initial state before _and_ after the interaction that causes state to update. For example, in `ParlorCard` the test for on line 68 should be rewritten as follows:

```js
 it('should change ParlorCard details state to true when the getParlorDetails method is called', () => {
      expect(wrapper.state()).toEqual({details: false})
      wrapper.find('.parlor-details').simulate('click')
      expect(wrapper.state('details')).toEqual(true)
  });
```
* Some inconsistencies in using snapshot to test components
* No tests for `CardContainer`

------------------------------------------------------------------

## Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.

* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 

* [x] Proficient - Everyone in the group has an opporunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.

* [ ] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.


Comments:

- Great opening and gif - great ice breaker! 
- There are a lot of words on the first slide - err on the side of having bullet points 
- Was frightened when I saw the words "Live Demo" - glad to see that you have a recording of the app demo 
- Great job with making the presentation very conversational and natural
- Nice use of humour and keeping it lighthearted
- Would great to see examples of code in a slide
- Visuals for your challenges (code snippets - see above) would strengthen the presentation