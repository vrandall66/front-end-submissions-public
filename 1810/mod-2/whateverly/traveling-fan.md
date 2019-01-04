# Whateverly 
* Students: Eric Fitzsimons, Theo Bean, and Travis Gee
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

* Not sure that the content inside [this article](https://github.com/geet084/traveling-fan/blob/master/src/TeamIcon.js#L7) really represents an article. There's probably a more semantic tag you could use here, otherwise I'd stick with a div.

* [This method](https://github.com/geet084/traveling-fan/blob/master/src/Popup.js#L21-L23) is redundant. No need to create another custom method that just calls another one. In your render method, where you're actually invoking this, you could just directly invoke `this.props.showAllTeams()` instead.

* Conditional logic [here](https://github.com/geet084/traveling-fan/blob/master/src/Popup.js#L36-L63) seems like it could be simplified...there is such a small amount of data that actually changes (just the key prop?) and the Card/City components also have a lot of shared JSX. 

* I'm concerned about your use of h1 and h2 tags [here](https://github.com/geet084/traveling-fan/blob/master/src/Card.js#L16-L28) these should be reserved for top-level application headings and subheadings. I would go back to some Mod 1 lessons and brush up on semantic use of HTML tags.

* [This](https://github.com/geet084/traveling-fan/blob/master/src/City.js#L18-L24) is a bit more logic than I'd like to see within a map inside of your render (maps inside of renders should generally stick to just returning a component on each iteration). I'd create a custom method that returns the data you want to map over exactly as you need it so that you can simplify what you're iterating over here.

* You have a bit of duplicate state [here](https://github.com/geet084/traveling-fan/blob/master/src/App.js#L11-L16) -- what's the difference between nflTeams and allTeams? nflCities and cities? The more duplicate state you have, the more places you're going to have to update things when they change. It gets very difficult to keep your state in sync when you do this, and makes your app much more prone to bugs. Try to avoid putting any sort of "derived" data in state and just modify your teams when and where you need to.



------------------------------------------------------------------

## GitHub Collaboration/Workflow

* [ ] Novice - Developers do not tag instructors in the two required PRs by due dates listed in the project outline or tagged PR has fewer than 200 lines of code. The developer creating the PR does not summarize the changes or why the changes were made. Reviewers are not leaving line-by-line feedback/comments _or_ are merging the PR before changes are made.

* [x] Advanced Beginner - Developers tag instructors in both required PRs by due dates _or_ in one of the two required. PR has less than the required lines of code in PR. Reviewers do not leave line-by-line feedback. May be merging PR before feedback is incorporated.

* [ ] Proficient - Developers tag instructors in both required PRs by due dates. PR is between 350 - 450 lines of code. The developer creating the PR summarizes the changes made, why those changes were necessary, and asks for insights. Reviewers leave line-by-line comments/feedback and wait to merge PR until feedback is incorporated.

* [ ] Exceptional - Meets all expectations for `Proficient`. The feedback is both kind _and_ insightful. There may be numerous threads of conversation where developers go back and forth to find the best solution to the problems they are solving together.


Comments:

Contribution breakdown:  
Travis: 56 commits  
Eric: 25 commits  
Theo: 23 commits  

- Looking at contributions in a group of three (comparing commits as well as actual code/features added) the split of the work does not seem balanced.
- Make sure that you are giving the _why_ behind your PR. Majority of PRs has no description of what has changed and needs reviewing or simply asks reviewiers to check things out or have a look at things (not being specific on what has changed or why). A lack of direction from the person requesting a review/help makes it infinitely more difficult for a reviewer to give a good review.
- Work on giving critical, constructive feeback to make the applicaiton better - many line-by-line comments simply compliment what has been done.
- Tagged instructors 12/19, 12/29, and 1/2. Lines of code submitted: under 100, around 300, and over 5000 with snapshots.

------------------------------------------------------------------

## Testing

* [ ] Novice - There is little or no evidence of testing in the application.

* [ ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The applicaiton contains numberous holes in testing and/or many features are untested.

* [ ] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features.

* [ ] Exceptional - Project has a running test suite that exercises the application used Enzyme. The test suite covers almost all aspects of the application.


Comments:

- Per the history, no contributions were found from Theo for testing. It is important that all group members make sure that every member on the project has the opportunity to test.






------------------------------------------------------------------

## Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.

* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 

* [x] Proficient - Everyone in the group has an opporunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.

* [ ] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.


Comments:


- Nice job with a live recording of the application!!
- Appreciate Eric dressing up a bit for the presentation - shows professionalism and the desire to impress. This doesn't mean you have to dress to the nines - but generally you want to dress slightly better than your audience when presenting
- Try not to stare at the ground as your other group members are speaking
- Pay attention to your body language while presenting. Hands in pockets comes off as too relaxed while crossed arms can seem standoffish
- Really enjoyed the addition (along with the visual) regarding the evolution of the application and how you made changes to your architecture
- Be sure to use technical terms as much as possible when describing the code that created.
- Avoid saying things like "we are just trying to just get this presentation out of the way." Showing off your project is a great way to show your passion about what you've created and statements like that give off the impression that you're not excited