# Game Time
* Students: Quin Hill & Alan Charles
* Evaluator: Cody Sehl
* Repo: https://github.com/abomb14c/game-time-BO

### Functional Expectations

✓ Game works, is clear
- Issue when the game speeds up, multiple bricks are broken

Score: 3

* 3 - Application is fully playable without crashes or bugs

### User Interface

✓ Interface clear, score makes sense
✓ Good game screens

Score: 3

* 3 - The application has many strong pages/interactions, but a few holes in lesser-used functionality.

### Testing

- Test naming - be sure to include the action you're testing and the result
- Tests in Ball-test.js test more than one thing
- Test velocity explicitly in `it should move` test
- Nitpick: combine constructor parameter tests in Game-test.js into one test

Score: 2-3

* 3 - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.
* 2 - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.

### JavaScript Style

- Game.blockCollision is pretty complex, consider making conditionals into their own variables
- Move some of the expressions (lines 144-147) into their own function(s)

Score: 3

* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.

### Application Organization

- Ball.moveBall function takes the game object
- Good use of inheritance

Score: 3

* 3 - Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.

### Workflow

✓ Git commits farily small
✓ PRs have few commits
✓ Use of branches

Score: 3

* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.
