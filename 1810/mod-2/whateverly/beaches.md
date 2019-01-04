# Whateverly 
* Students: Libby Yeh, Kristen Hallstrom, Elly Torres
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

* [x] Advanced Beginner - The application may be confusing or difficult to use at times. The application shows effort in the interface, but the result is not effective because UX and/or UI still present an application that is incomplete or difficult to use. It is not clear that the user stories helped to guide UX.

* [x] Proficient - The application has many strong pages/interactions. The application can stand on its own to be used by instructor without guidance from a developer on the team.

* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, the application is fully responsive, and has clearly had special consideration around usability on devices. There no holes in functionality.


Comments:

* Doesn't appear like the filtering is working to change the beaches that are displayed by county after you do your first round of filtering

* Difficult to read the 'Find your happy place' button with the white text and the glare of the sun from the background -- I think the sizing is a bit off overall as well, you should test this a bit further in different screen sizes and check up on the responsiveness. On my laptop I'm seeing a lot of horizontal scrolling that we'd like to avoid

* The maps section is helpful, but I feel like I should be able to click on something here. It's unclear to me that I can't view more information about a beach that appears on the maps here. With the separation of beaches and maps, I have to go back and forth between the Beaches and Maps pages. I'd like to see the beach and where it is simultaneously.

* The click targets for the beach cards are much too tiny -- I should be able to click anywhere on that entire little card, rather than just on the title of the beach

* I would put some sort of semi-opaque overlay on the rest of the site after a user clicks on a particular beach and gets that pop-up of extra details. It's a little overwhelming having so much content so clearly visible, I'd like that pop-up to stand out a little bit more

* I'd like to see a few more hover effects or indicators of the things I can/can't click on in the app. Generally, at minimum, anything that can be clicked on should turn the cursor into a little hand (like it does for regular hyperlinks)

* The hero image is nice in terms of getting the user’s attention.







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

* Using state to explicitly decide which components should be rendered, like you're doing [here](https://github.com/libbyeh/beaches/blob/master/src/App.js#L7-L32), is an anti-pattern. You want to conditionally render components based on user interactions, not explicit instructions that say "render this component just because state says so". e.g. if a user has selected a county, we should be showing the beaches component with those matching beaches. In which case, our state would say something like:

```
userSelectededCounty: 'Santa Barbara'
```

and our render method of our App would say something like:

```
this.state.userSelectedCounty ? <Beaches county={this.state.userSelectedCounty} /> : <LandingPage />
```


* The [header](https://github.com/libbyeh/beaches/blob/master/src/Maps.js#L13-L15) is something that should belong in your App component, since it's going to be rendered all the time no matter what. It's not specific to the maps page or the beaches page. If you need to adjust the way it looks based on which component is showing, you can just style it differently with CSS.

* [This](https://github.com/libbyeh/beaches/blob/master/src/Maps.js#L20-L44) looks like a good use-case for passing in a prop that is an array of all the beach counties, and looping over that array to render the map for each county.

* Seems weird for this [landing page component](https://github.com/libbyeh/beaches/blob/master/src/LandingPage.js#L8-L18) to have it's own state of `landingPage` that gets toggled true or false. This should be a stateless component with no conditional rendering. The render method should simply return what the landingPage component would look like. Then, in your App component, you would do some conditional logic to determine if you should be rendering the landingPage or some other component.

* Again, we don't want to be doing conditional rendering for our components like [this](https://github.com/libbyeh/beaches/blob/master/src/BeachesCard.js#L9-L13), where we're rendering an empty div of nothing based on a condition. You should move this conditional logic to the parent component of BeachesCard so that the component doesn't even get mounted if the condition isn't met. Otherwise you are rendering empty components for no reason.

* Curious about the difference between [beaches and allBeaches](https://github.com/libbyeh/beaches/blob/master/src/Beaches.js#L11-L12) in your state. This seems redundant and appears that they represent the same thing after your initial [fetch](https://github.com/libbyeh/beaches/blob/master/src/Beaches.js#L23-L24)

* Nice tiny methods [here](https://github.com/libbyeh/beaches/blob/master/src/Beaches.js#L40-L54)

* You probably want to refactor this [method](https://github.com/libbyeh/beaches/blob/master/src/Beaches.js#L56-L71) so that you're only setting the state once at the very end of the function after you've determined all the beaches that need to be shown. Trying to set state on each iteration of filter is probably what's causing your bug where it doesn't work on the second attempt. Something like:

```
  let filteredBeaches = [];

  this.state.beaches.filter((beach) => {
    if (e.target.value === beach.county) {
      filteredBeaches.push(beach)
    }
  })

  if (!filteredBeaches.length) {
   filteredBeaches = this.state.allBeaches
  }

  this.setState({
    beaches: filteredBeaches
  })
}
```






------------------------------------------------------------------

## GitHub Collaboration/Workflow

* [ ] Novice - Developers do not tag instructors in the two required PRs by due dates listed in the project outline or tagged PR has fewer than 200 lines of code. The developer creating the PR does not summarize the changes or why the changes were made. Reviewers are not leaving line-by-line feedback/comments _or_ are merging the PR before changes are made.

* [x] Advanced Beginner - Developers tag instructors in both required PRs by due dates _or_ in one of the two required. PR has less than the required lines of code in PR. Reviewers do not leave line-by-line feedback. May be merging PR before feedback is incorporated.

* [ ] Proficient - Developers tag instructors in both required PRs by due dates. PR is between 350 - 450 lines of code. The developer creating the PR summarizes the changes made, why those changes were necessary, and asks for insights. Reviewers leave line-by-line comments/feedback and wait to merge PR until feedback is incorporated.

* [ ] Exceptional - Meets all expectations for `Proficient`. The feedback is both kind _and_ insightful. There may be numerous threads of conversation where developers go back and forth to find the best solution to the problems they are solving together.
Comments:

Contribution breakdown:  
Libby: 29 commits  
Elly: 34 commits  
Kristen: 20 commits  

- A few times where creator of PR is asking explicit questions around the proposed changes (which is good); however, there is not a response or exchange between developers. 
- A numbers of PRs with no comments from reviewers - PRs are just merged. A few that state that code was written together... making it unclear as to why a PR was submitted in the first place.
- Tagged instructors 1/2, 12/20, and 12/22. Each PR was less than 100 lines of code to review.

------------------------------------------------------------------

## Testing

* [ ] Novice - There is little or no evidence of testing in the application.

* [ ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The applicaiton contains numberous holes in testing and/or many features are untested.

* [ ] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features.

* [ ] Exceptional - Project has a running test suite that exercises the application used Enzyme. The test suite covers almost all aspects of the application.


Comments:










------------------------------------------------------------------

## Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.

* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 

* [x] Proficient - Everyone in the group has an opporunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.

* [ ] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.

Comments:

- Make sure that you are consistently speaking clearly and loudly
- Nice job with showing why there isn't specific information available for beaches and how your app solves this problem
- Skip going over the tech stack - know your audience and make sure that you are presenting/crafting your presentation for them
- Nice job using a recording of app interactions
- Make sure that you are articulating the code examples. There were a few instances that you were speaking about your code and not using technical terms to articulate things - which would improve the presentation.