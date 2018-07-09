# Game Time
* Students: Michael and Paul
* Evaluator: Brittany Storoz

Comments:
* Variable/method naming needs a little work -- some properties like `keyPressed` and `stopped` vs `paused` vs `isGameOver` add a little confusion to understanding the code from an outsider's perspective
* Some room for refactoring and moving methods/properties onto other classes -- demonstration of OOP is mostly there, but could use a little clarification.

### Functional Expectations

* 4 - Application is fully playable and exceeds the expectations set by instructors

* github pages deploy & level up extensions complete, nice!

### User Interface

* 3.5 - The application has many strong pages/interactions, but a few holes in lesser-used functionality.

* Little difficult to tell when the scores were updating on each collision

* Nitpick about the skewing of the trails vertically vs. horizontally


### Testing

* 3 - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.

* How big [this](https://github.com/michaelyons/game-time/blob/master/test/Game-test.js#L9-L60) object is that you're trying to assert against should be an indicator that your Game class is keeping track of way too many things.

* I'd break up [this](https://github.com/michaelyons/game-time/blob/master/test/Game-test.js#L26) it block into two separate ones. One that asserts that the players have been drawn, and one that asserts the move method actually updates their x and y coordinates. For testing the move method, you'd also want to assert a starting x/y, then call move, then assert the final x/y so that you can tell those values were actually updated and I don't have to guess where the initial x/y values were.

* You're adding a bit too much logic in all of your tests. You want to call as few methods and set as few properties as possible in your tests so that you can really isolate your assertions to test a single thing. In a test like [this](https://github.com/michaelyons/game-time/blob/master/test/Game-test.js#L233), you're recreating the entire flow of the game. If this test fails, figuring out where it went wrong would be really difficult because you are calling so many methods. You should be able to simply set a player's score to 3 then check that `gameOver` is true.

### JavaScript Style & OOP

* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.

* You should probably have a `Player` class that inherits from the GamePiece, and adds a `trail` property that's made up of `GamePieces`. The trails are currently on your `Game` class, but each trail is specific to a single player - so they should be on a `Player` class instead. Same with each player's score. Those are specific to a player, not the game itself.

* Storing your players in an array would allow you to reduce a lot of repetitive code in places like [this](https://github.com/michaelyons/game-time/blob/master/lib/Game.js#L26) and [this](https://github.com/michaelyons/game-time/blob/master/lib/Game.js#L102-L122). You could `forEach` over them to apply values and call methods on each one.

### Workflow

* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.

* Paul's commit messages could use a little work, consistency and style is important even in those. 

* [NO CURSING](https://github.com/michaelyons/game-time/commit/36ae3b11a39221d86a7791dd9a2948aec6f5f155), also this commit is doing a little too much. Add the game class file stubbed out with just a class and a constructor (nothing in it), and import it to your index. Then commit. Don't add all this commented out code and other changes to the index file within this commit.