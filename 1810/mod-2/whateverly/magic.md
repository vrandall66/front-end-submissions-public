# Whateverly 
* Students: Dylan Hofmann, Jeo D, Hillary Stewart, and David Cisneros
* Evaluator: Brittany, Pam, and Robbie

# Rubric

## Specification Adherence

* [ ] Novice - README is missing or incomplete. Codebase is not organized. User stories from group are never submitted. Application does not solve the presented problem.

* [ ] Advanced Beginner - README is complete. Codebase is organized. User stories are completed; however, may be late. Some user stories may be unclear or hard to understand. Application is close to solving presented problem.

* [x] Proficient - Developers turn in user stories on time and iterate on user stories throughout the life of the project, as needed. User stories have enough detail - such that an outside developer could jump right in and help with user stories/tickets. Application solves the presented problem.

* [ ] Exceptional - Meets all expectations for `Proficient`. Developers may use personas to help guide their user stories. Developers may also incorporate other tools to assist in planning - workflow diagrams, story maps, etc.


Comments:

* With so many moving pieces in this app, it would be better to have a gif compared to screenshots, but the screenshots are nice.
* In the future, break out your user stories into multiple issues so each issue can be tackled independently.

------------------------------------------------------------------

## UI/UX

* [ ] Novice - The application is confusing or difficult to use. The final project presents an interface that is incomplete.

* [ ] Advanced Beginner - The application may be confusing or difficult to use at times. The application shows effort in the interface, but the result is not effective because UX and/or UI still present an application that is incomplete or difficult to use. It is not clear that the user stories helped to guide UX.

* [x] Proficient - The application has many strong pages/interactions. The application can stand on its own to be used by instructor without guidance from a developer on the team.

* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, the application is fully responsive, and has clearly had special consideration around usability on devices. There no holes in functionality.


Comments:

* Some left padding needed on the input/results.
* Autocomplete is a really nice feature when there are so many options for cards.
* The button size for increasing or decreasing card number might be too small for mobile. It's also _ver_ close to the trash icon, which is a destructive action and might be clicked accidentally.
* The card is still very small in the popup - should I be able to read the text on the card? It's very small.
* The plain background where the cards a placed is nice. Good to keep that simple to see the cards clearly.




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

* [x] Advanced Beginner - There is some duplication and there may be one or two major bugs. The application has large components and logic could be broken apart into smaller, stateless components. JavaScript may be hard to read/follow.

* [ ] Proficient - Application has little to no duplication and no major bugs. Application has several components built out that logically break apart the functionality. JavaScript may be hard to follow at times but is generally easy to read/understand. 

* [ ] Exceptional - Application has exceptionally well-factored code with little or no duplication and all components separated out into logical components. There are zero instances where an instructor would recommend taking a different approach to design and component architecture. DRY and SRP (Single Responsibility Principle) practices are incorporated, making JavaScript very easy to follow/read.


Comments:

* There's a *lot* of duplicate code throughout the repo, and you're not leveraging the fact that React allows you to create **reusable** components. Look at how incredibly similar your [CardListItem](https://github.com/dForDeveloper/magic-whateverly/blob/master/src/CardListItem/CardListItem.js) and [WishListItem](https://github.com/dForDeveloper/magic-whateverly/blob/master/src/WishListItem/WishListItem.js) components are. These should be a single component that varies just slightly based on whether it belongs to your wish list or your card list (if that even matters within this component!) Same thing with your CardList and WishList components -- they are too similar to warrant completely separate components. You could probably also combine your FaveListItem and FaveList components with a little conditional rendering logic. With the structure of your app, I'd say you should have two components instead of the 6 I just mentioned: a List component and an Item component that can both be flexible enough to handle a card/wish/favorite. You're doing a lot more work duplicating these components when they should be shared and reused as much as possible. 

* [This](https://github.com/dForDeveloper/magic-whateverly/blob/master/src/Header/Header.js#L4-L29) could be refactored quite a bit. You don't need all these separate methods that are calling the same functions. Just call them directly in your render method with the appropriate arguments. e.g.:

```
<ul className="header--ul">
  <li onClick={() => this.props.setAsideView('cardList')} className="my-cards">My Cards</li>
  <li onClick={() => this.props.setAsideView('faveDecks')} className="fave-decks">Saved Decks</li>
  <li onClick={() => this.props.setAsideView('wishList')} className="my-wish-list">Wish List</li>
</ul>
```

* A little odd to have two methods [here](https://github.com/dForDeveloper/magic-whateverly/blob/master/src/Deck/Deck.js#L5-L12) where one is named after what's actually happening (adding a favorite to the deck) and one is just telling you that a click event occurred (handleClick). I prefer the former naming convention, but if you're going to use `handleClicks`, I'd be consistent and use them everywhere. 

* I'd move this [localStorage](https://github.com/dForDeveloper/magic-whateverly/blob/master/src/App/App.js#L12-L20) logic into your `componentDidMount` method rather than having it in the constructor. Let your state be full of empty arrays to start, and update it with values from localStorage as they become available.

* Overall the code is pretty over-engineered and difficult to follow. I'd say you've written more than double the amount of code you actually needed in order to accomplish the functionality of your app. Getting some more experience with the benefits of React will help you recognize patterns that will allow you to simplify your logic and cut down on the amount of code you're writing.





------------------------------------------------------------------

## GitHub Collaboration/Workflow

* [ ] Novice - Developers do not tag instructors in the two required PRs by due dates listed in the project outline or tagged PR has fewer than 200 lines of code. The developer creating the PR does not summarize the changes or why the changes were made. Reviewers are not leaving line-by-line feedback/comments _or_ are merging the PR before changes are made.

* [x] Advanced Beginner - Developers tag instructors in both required PRs by due dates _or_ in one of the two required. PR has less than the required lines of code in PR. Reviewers do not leave line-by-line feedback. May be merging PR before feedback is incorporated.

* [x] Proficient - Developers tag instructors in both required PRs by due dates. PR is between 350 - 450 lines of code. The developer creating the PR summarizes the changes made, why those changes were necessary, and asks for insights. Reviewers leave line-by-line comments/feedback and wait to merge PR until feedback is incorporated.

* [ ] Exceptional - Meets all expectations for `Proficient`. The feedback is both kind _and_ insightful. There may be numerous threads of conversation where developers go back and forth to find the best solution to the problems they are solving together.


Comments:

Contribution breakdown
Jeo: 63 commits  
Dylan: 54 commits  
Hillary: 38 commits  
David: 11 commits  

- Looking at contributions in a group of four (from commits as well as actual code/features added) the split of the work does not seem balanced.
- There is a fair amount of conversation happening between devs submitting PRs and those reviewing. Still a number of 
- Tagged instructors on  12/26, 12/27, 12/28, 12/29, 12/31, and 1/2. Each PR was less than 100 lines of code to review.

------------------------------------------------------------------

## Testing

* [ ] Novice - There is little or no evidence of testing in the application.

* [x] Advanced Beginner - Project has sporadic use of tests at multiple levels. The applicaiton contains numberous holes in testing and/or many features are untested.

* [ ] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features.

* [ ] Exceptional - Project has a running test suite that exercises the application used Enzyme. The test suite covers almost all aspects of the application.


Comments:

* Really good coverage with snapshot testing
* Overall the majority of tests for the application are snapshots or testing for whether functions or mocked methods have been called. In order to create a more robust test suite some recommendations are as follows:  
  - Additional assertions could be added to make sure that mock functions are being called a set number of times when a method is invoked. Also be sure to test with `toHaveBeenCalledWith()` when you are passing arguments to these mocked functions  
  - If a method is returning a value (like in `updateUsersCardData`) be sure that you are also testing for that returned value. Same goes for any methods with conditional logic - always be sure that you test both possible "paths" in a method  
  - Create a separate it block for testing for default state and be sure that you are testing for updates to state that are triggered by methods  

------------------------------------------------------------------

## Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.

* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 

* [ ] Proficient - Everyone in the group has an opportunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.

* [x] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.


Comments:

- Opening is great - funny and captured the audience's attention right away!
- Good amount of eye contact and confidence in speaking. Body language for the entire group is pretty consistently relaxed but confident.
- Appreciate the history of what makes this app useful
- Slides and visuals are on the slides are super useful - especially like how the components that held state are highlighted in blue
- Nice job with the recording of the app and not doing a live demo
- Great job articulating some of the features