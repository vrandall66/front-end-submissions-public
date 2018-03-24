# Game Time
* Students: Cam Buscher & Krista Handel
* Evaluator: Cody Sehl
* Repo: https://github.com/YayFiber/game-time

### Functional Expectations

- Good game!

Score: 3

* 3 - Application is fully playable without crashes or bugs

### User Interface

- UI makes sense!

* 3 - The application has many strong pages/interactions, but a few holes in lesser-used functionality.

### Testing

✓ Opinion: Can combine multiple tests about constructor into one test
✓ Consider making test names more explicit by including the action you're testing and the result of that action
✓ In game-test.js, 'should bounce off paddle', you don't need the first assert (because you specify the value in the constructor), you don't need to set `ball.dy` to the result of the function you're testing, you can just create a new variable and assert against that.

Score: 3

* 3 - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.

### JavaScript Style

✓ Think about refactoring createBricks into a few smaller functions

Score: 3

* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.

### Application Organization

- Brick class has many bricks
✓ Game takes a ball and a paddle? -- that's okay
- Move your document/context stuff out of the game loop in index.js (alternately, move all of the game stuff down into game.js)
- Files that represent classes should be capitalized
✓ bricks.js -> brick.js In OOP classes should refer to singular entities. Rework 'bricks' to be singular and move the list abstraction up somewhere else

Score: 3

* 3 - Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.

### Workflow

✓ Used GitHub issues
- Keep working on Git knowledge

Score: 3

* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.
