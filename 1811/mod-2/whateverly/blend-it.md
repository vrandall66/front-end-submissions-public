# Whateverly 
* Students:
* Evaluator:
* Repo: https://github.com/easbell/Blend-It

# Rubric

## Specification Adherence

* [ ] Novice - README is missing or incomplete. Codebase is not organized. User stories from group are never submitted. Application does not solve the presented problem.

* [ ] Advanced Beginner - README is complete. Codebase is organized. User stories are completed; however, may be late. Some user stories may be unclear or hard to understand. Application is close to solving presented problem.

* [X] Proficient - Developers turn in user stories on time and iterate on user stories throughout the life of the project, as needed. User stories have enough detail - such that an outside developer could jump right in and help with user stories/tickets. Application solves the presented problem.

* [ ] Exceptional - Meets all expectations for `Proficient`. Developers may use personas to help guide their user stories. Developers may also incorporate other tools to assist in planning - workflow diagrams, story maps, etc.


Comments:




------------------------------------------------------------------

## UI/UX

* [ ] Novice - The application is confusing or difficult to use. The final project presents an interface that is incomplete.

* [ ] Advanced Beginner - The application may be confusing or difficult to use at times. The application shows effort in the interface, but the result is not effective because UX and/or UI still present an application that is incomplete or difficult to use. It is not clear that the user stories helped to guide UX.

* [ x ] Proficient - The application has many strong pages/interactions. The application can stand on its own to be used by instructor without guidance from a developer on the team.

* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, the application is fully responsive, and has clearly had special consideration around usability on devices. There no holes in functionality.


Comments:

* Dig the color scheme, it's nice to see something other than blue :) 

* I like the script font reserved specifically for the title -- I would maybe put the subtitle in a slightly more readable font, but pairing this with the Open Sans is nice. Overall I think we could have just slightly more differentiation in headings vs. basic text. e.g. a different font for the ingredient selections vs. the ingredient category titles; 'matching smoothie recipes' heading vs. the name of the smoothies that actually appear; etc. We can differentiate by incorporating another font, or simply adjusting the boldness/size of the pre-existing font. This will help make the hierarchy of content a little more obvious. Right now it looks like there are a couple of different pieces of content competing for my attention.

* Nice handling of clicking into a recipe and being able to head back to the full list - but it appears like I can click anywhere in the recipe to send myself back? (I don't have to just click directly on the back to results link.) This is a more common pattern when you have a popup/modal window of some sort, but is a little disorienting here since it looks like we're navigating to a totally new page. 







------------------------------------------------------------------

## CSS/Sass Style

* [ ] Novice - There are several (10+) instances of duplication and one or two major bugs. Developers write code with unnecessary selectors or tags which do not increase clarity.

* [ ] Advanced Beginner - There is some duplication (5-10 instances) in the codebase. There may be one to two minor bugs. There may be some unnecessary selectors or tags. Application adds organization for the whole stylesheet and within rules.

* [ x ] Proficient - Application is thoughtfully put together with comments to help guide organization. There may be some duplication (fewer than 5 instances) present. Comments are present to assist with organization of code.

* [ ] Exceptional - Meets all expectations for `Proficient`. The application has exceptionally well-factored CSS/Sass with all styles separated out into logical stylesheets. There are zero instances where an instructor would recommend taking a different approach.


Comments:

* Nice job pulling your variables out into their own scss file so they only need to be updated in one spot. If you could be just slightly more generic with your color variable names, that would be helpful. e.g. title-color-teal --- what happens if you rebrand/redesign your app and your color scheme no longer uses teal? Now instead of just having to update the value, you have to update the variable name as well in any file that references it.

* Font families would be another good thing to pull out into variables as you're referencing them in multiple places at the moment. Will also make it easier to update the fonts later on if you tweak them.


* I'd recommend looking into strategies for ordering your CSS properties -- the most common I've seen in the wild is ordering them by type as described in [this](https://css-tricks.com/poll-results-how-do-you-order-your-css-properties/) blog post. (I'm shocked that 'randomly' is so high in those poll results, because I've never worked on a team that accepted that.) 





------------------------------------------------------------------

## JavaScript / React Style

* [ ] Novice - There is a significant amount of duplication and one or two major bugs. JavaScript does not follow the principles of `DRY` (Don't Repeat Yourself)

* [ ] Advanced Beginner - There is some duplication and there may be one or two major bugs. The application has large components and logic could be broken apart into smaller, stateless components. JavaScript may be hard to read/follow.

* [x] Proficient - Application has little to no duplication and no major bugs. Application has several components built out that logically break apart the functionality. JavaScript may be hard to follow at times but is generally easy to read/understand. 

* [ ] Exceptional - Application has exceptionally well-factored code with little or no duplication and all components separated out into logical components. There are zero instances where an instructor would recommend taking a different approach to design and component architecture. DRY and SRP (Single Responsibility Principle) practices are incorporated, making JavaScript very easy to follow/read.

Comments:

* Quite a few places arrow syntax is being used unnecessarily
* Be mindful of readability when making use of destructuring for your props. You'll most often see destructuring happening within the render method (where you are often trying extract multiple properties to render) as a way to clean up your code. [Destructuring this method here](https://github.com/easbell/Blend-It/blob/master/src/Smoothie.js#L6-L7) did not add additional clarity/readability - instead, it had the reverse effect. This was compounded by the fact that the `showRecipe` method has the same naming as the state property of `showRecipe` within `SmoothieContainer`. 
* - Opportunities for refactoring renders within the components - lots of conditions that make it hard to read/follow.


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

* [ ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested.

* [ ] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features.

* [ ] Exceptional - Project has a running test suite that exercises the application used Enzyme. The test suite covers almost all aspects of the application.


Comments:










------------------------------------------------------------------

## Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.

* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 

* [X] Proficient - Everyone in the group has an opportunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.

* [ ] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.


Comments:

* Good app demo - tighten it up a little bit. We don't need to know every detail of the app - give us more of a high level overview and then dive into details if they are important (consider pre-made gifs to speed things up too).
* Liked the lessons learned from the user experience section, before and after screenshots/gifs were great







