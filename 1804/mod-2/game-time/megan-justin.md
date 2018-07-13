# Game Time
* Students: Justin & Megan
* Evaluator: Pam Lovett

### Functional Expectations

* 3 - Application is fully playable without crashes

- Bug - frog being "invincible" in the water
- Multiple levels of difficulty in app

### User Interface

* 3 - The application has many strong pages/interactions, but a few holes in lesser-used functionality.

- Words on the screen are hard to read due to typeface and colors
- No difficulty in using the application or understanding the rules of the game
- Think about adding directions as to what arrow keys to use
- Clear indication/directions of dying and when game is over

### Testing

* 3 - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.

- ESLint showing 6 complaints
- Some features (namely functionality that is not working properly) not being tested

### JavaScript Style & OOP

2.5

* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.
* 2 - Your application has a significant amount of duplication and one or more major bugs. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. There are one or more major bugs.


- Duplicated code: Car, Froggy, and Log will inherit `isCollidingWith` from `Gamepiece`
- In `Froggy.js` the properties of `dx`, `dy`, and `dxv` shoudl not be set in the constructor but in `super()` so they will inherit from the parent
- Overall, majority of code is easy to follow


### Workflow
* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.

- Would like to see more than 90 commits - should have more given the scope of project
- Nice job with commit messages - some could be a bit more descriptive in the body of the commit. Several instances of `adding functionality` with no other explanation. What functionality did you add? Why?
- Would like to see more issues/progress logged 
