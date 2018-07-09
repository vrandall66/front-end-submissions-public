# Game Time
* Students: Benjamin and Gray
* Evaluator: Brittany Storoz

Comments:
* Testing it block descriptions could be a bit more accurate -- focus more on what the code is doing. What methods are being called and what values are updating.
* Code is clean, readable and stylistically consistent. Some opportunities for refactoring but overall demonstration of skills is there.

### Functional Expectations

* 4 - Application is fully playable and exceeds the expectations set by instructors

* level up + github pages extensions complete, nice!

### User Interface

* 3.75 - The application is pleasant, logical, and easy to use. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer.

* Just little nitpicks like the font being a little difficult to read, but lots of nice UI effects and clear instructions

### Testing

* 3 - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.

* You also want to assert that your `tail` is an instance of the `Tail` class [here](https://github.com/gray-smith/gs-bp-game-time/blob/master/test/Tail-test.js#L6-L8). You can import `expect` from chai and test something like: `expect(tail).to.be.an.instanceof(Tail);`

* I would combine all of [these](https://github.com/gray-smith/gs-bp-game-time/blob/master/test/Tail-test.js#L11-L35) instance property checks into a single it block with a description like 'should set initial instance properties'

* Break out this context [setup](https://github.com/gray-smith/gs-bp-game-time/blob/master/test/Player-test.js#L7-L19) into it's own file (it could be in a /test/mocks/ directory) so that you don't have to repeat that setup in every test file and you can just import it instead

* [This](https://github.com/gray-smith/gs-bp-game-time/blob/master/test/Player-test.js#L25-L27) doesn't really test that a new player was instantiated. It's asserting that it has an x value of 100. You don't want to write tests that make someone have to 'infer' that things succeeded. Assert instead that player exists, is an object, and an instance of the Player class.

* You might want to add an initial assertion [in these tests](https://github.com/gray-smith/gs-bp-game-time/blob/master/test/Player-test.js#L55-L57) that verifies the x position starts at 100, then call move, then assert that it equals 110. I can infer that it starts at 100 from some of your previous tests, but every test should be able to stand on its own to be read by another developer.

* Assert that both of [these players](https://github.com/gray-smith/gs-bp-game-time/blob/master/test/Game-test.js#L41) are instances of the Player class. You could have an array of players with a length of two but maybe both of those values are null for some reason. Assertion needs to be a bit more specific. 

* [This](https://github.com/gray-smith/gs-bp-game-time/blob/master/test/Game-test.js#L44) isn't checking whether the game is over or not, it's asserting that when `isGameOver` is called, the `gameOver` instance property is changed to true. You should also assert that it's false first and the method actually swaps it to true.

* [This](https://github.com/gray-smith/gs-bp-game-time/blob/master/test/Game-test.js#L58) is also a little off -- you're asserting that a new level resets the player's values. What else does it do? Does it update `this.level` each time it's called?

### JavaScript Style & OOP

* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.

* Since you're resetting the players array in `isGameOver`, and you're not calling `loadPlayers` anywhere else, you could just reassign `this.players` to an array like `this.players = [playerOne, playerTwo]` instead of pushing them in [separately](https://github.com/gray-smith/gs-bp-game-time/blob/master/lib/Game.js#L22-L23)

* [This](https://github.com/gray-smith/gs-bp-game-time/blob/master/lib/Game.js#L103) reads a little weird to me. Maybe it's the collision detection that was set up for you - but the way I read this conditional is that if player 1 is *not* colliding with the canvas object, update player 2's score. I'm confused why there's a bang in front of the conditional. Does `isCollidingWith` return true if the first object is colliding with the object passed in? Or false?

* Be consistent with the naming of your players, you have `player1` and `player2` [here](https://github.com/gray-smith/gs-bp-game-time/blob/master/lib/Game.js#L95) but `playerOne` and `playerTwo` elsewhere. It might make someone think they refer to different values.

* I would refactor your [initial tail setup](https://github.com/gray-smith/gs-bp-game-time/blob/master/lib/Tail.js#L11-L18) to include `this.tails = this.setInitialTail()` in the constructor, then have `setInitialTail` return `[new Tail(x, y, SCL, SCL, color)]`. By just calling that method in the constructor, it's difficult to tell that `this.tails` is going to be an instance property. You want to make sure anything you set as an instance property is up top in that constructor so other developers are aware of what kind of data the class is keeping track of. It gets a little lost when it's buried in a method like that. Also, passing in SCL and SCL twice in your `new Tail` call looks like a mistake. I'd explicitly pass in a height and width, even if they were the same pixel value. 

* You won't normally see variable values start with an uppercase letter like [Left, Right, Up, Down](https://github.com/gray-smith/gs-bp-game-time/blob/master/lib/Tail.js#L33-L42). Remember capitalized initial letters are reserved for denoting when something is a class and should be instantiated with the `new` keyword. Don't use that convention for anything else.

### Workflow

* 4 - The developer/team effectively uses Git branches and many small, atomic commits that document the evolution of their application with descriptive commit messages. The team displays good pairing practices (driver-navigator, dividing up work, etc) and utilizes some sort of planning tool (GitHub issues, Waffle, Trello, etc). The team develops a clear MVP (minimum viable product) and conducts a DTR (define the relationship). Both members contribute meaningfully to the application.
* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.
* 2 - The developer/team makes large commits covering multiple features that make it difficult for the evaluator to determine the evolution of the application. The team does not utilize a planning tool or equitable pairing practices. One or both members do not contribute meaningfully to the application.
* 1 - The developer/team committed the code to version control in only a few commits. The evaluator cannot determine the evolution of the application.
* 0 - The application was not checked into version control.

* Nice readable and consistent commit messages



<!-- * **Public directory**

* **Find in array for declare winner**

* **NewLevel** -->