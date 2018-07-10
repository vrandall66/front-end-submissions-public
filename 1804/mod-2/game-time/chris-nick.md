# Game Time
* Students: Chris & Nick
* Evaluator: Pam Lovett

### Functional Expectations

* 3.5 - Application is fully playable without crashes or bugs

- Extension - up and running on GitHub pages!
- Minor bug (that is listed in issues) concerning the snake being able to eat food that it passes (without colliding)


### User Interface

* 4 - The application is pleasant, logical, and easy to use. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer.

- Love the UI AND those angled divs. As we discussed, may not want to create an app that plays music automatically. At the very least, make sure the user has the option to shut off the music near the top of the screen
- Appreciate that the game is the centerpeice of the the app and that additional info can be found further down.
- May want to consider adding something that says `Click to Start` as it was not obvious that the start button should be clicked. It does not look like a button and the previous instructions are all related to the keyboard.

### Testing

* 3 - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.

- ESLint shows ZERO complaints ----> WOOHOO!
- Tests missing for some methods/functionality - nothing to check the the snake growing, for food being created, etc

### JavaScript Style & OOP

* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.

- In `Food.js` the properties of `this.x = x` or `this.y = y` do not need to be set since you are inheriting these properties from your parent class (by way of `super()`)
- Overall, code is pretty easy to follow

### Workflow

* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.

- Good amount of commits - could use more considering scope of application. Be sure that your commit messages are answering not only WHAT but WHY. Lots of commits of `Fix ________` that are not very helpful - what exactly did you fix? Why? Or `Add test`... what test were you adding? 
- Quality of of commit messges started going down near the projects end. Be sure to stay consistent throughout.
- Nice job keeping track of issues/progress
