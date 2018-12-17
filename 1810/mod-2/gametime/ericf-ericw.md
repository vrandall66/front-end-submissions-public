# Game Time
* Students: Eric & Eric
* Evaluator: Brittany


### Functional Expectations

* 2.5 - Application is mostly playable, though with some bugs and slight functionality missing

* Quite a few bugs when trying to guess a letter / buy a vowel with very little indicator of what's going wrong -- is it a user error or is there a bug in the code? Makes it difficult to follow the flow on your own unless you've recognized the patterns of the buggy behavior.
* Bonus round not quite hooked up

### User Interface

* 3 - The application has many strong pages/interactions, but a few holes in lesser-used functionality.

* Overall the UI looks really nice, but it's difficult to tell what the user flow should be -- when can I spin? when can I buy a vowel? etc. Overall I think this can be fixed by adding some 'disabled'/'active' states to a lot of the UI elements that make them a little less prominent when it's not an option to interact with them, and make them more obvious when you should be interacting with them.
* Nice not allowing the game to start without player names but let's make that something other than an alert message in the future

### Testing

* 4 - Project has a running test suite that exercises the application at multiple levels. The test suite covers almost all aspects of the application and uses mocks and stubs when appropriate. ESLint shows 0 complaints.
* 3 - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.
* 2 - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.
* 1 - There is little or no evidence of testing in this application. ESLint shows 10+ complaints.

### JavaScript Style & OOP

* 4 - Application has exceptionally well-factored code with little or no duplication. SRP (single responsibility principle) and DRY (don’t repeat yourself) principles are utilized. There are zero instances where an instructor would recommend taking a different approach. Application is organized into classes (and correctly uses inheritance) and there are no instances where instructor would suggest moving logic or data to another class. The business-logic code driving functionality is cleanly separated from rendering, view-related code.
* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.
* 2 - Your application has a significant amount of duplication and one or more major bugs. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. There are one or more major bugs.
* 1 - Your client-side application does not function. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Application is not separated into classes, or methods and properties are illogically assigned to classes. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Business-side logic and view-related code is not separated at all.


### Workflow

* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.


* Mostly nice, consistent commit messages except for capitalization -- make sure your messages always start with a capital letter
* Generally a nice breakout of your commits, where they're not doing too much, but make sure that only relevant changesets make it into each commit. e.g. based on [this](https://github.com/ericweissman/wheel_of_fortune/commit/54bd8f08f81d177cacf93cf548672e3971272aba) commit message, I would expect that the index.html changes wouldn't be included there. That kind of change should go in a subsequent commit.
* You might want to look into `git squash` to merge some commits before you push them into master -- just a nice tool to be aware of. You can reduce duplicate commits (I noticed a couple) that do the same thing like 'Update README' (if you do this 5 times you can just squash it into a single commit when you're done that includes all the changes you made over all those commits)
