# Game Time
* Students: Michael and Paul
* Evaluator: Brittany Storoz

Comments:
* 
* Variable/method naming needs a little work -- some properties like `keyPressed` and `stopped` vs `paused` vs `isGameOver` add a little confusion to understanding the code from an outsider's perspective
* Some room for refactoring and moving methods/properties onto other classes -- demonstration of OOP is mostly there, but could use a little clarification.

### Functional Expectations

* 4 - Application is fully playable and exceeds the expectations set by instructors

* github pages deploy & level up extensions complete, nice!

### User Interface

* 4 - The application is pleasant, logical, and easy to use. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer.
* 3 - The application has many strong pages/interactions, but a few holes in lesser-used functionality.
* 2 - The application shows effort in the interface, but the result is not effective. The evaluator has some difficulty using the application when reviewing the features in the user stories.
* 1 - The application is confusing or difficult to use.

### Testing

* 3 - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.

* How big [this](https://github.com/michaelyons/game-time/blob/master/test/Game-test.js#L9-L60) object is that you're trying to assert against should be an indicator that your Game class is keeping track of way too many things.

* I'd break up [this](https://github.com/michaelyons/game-time/blob/master/test/Game-test.js#L26) it block into two separate ones. One that asserts that the players have been drawn, and one that asserts the move method actually updates their x and y coordinates. For testing the move method, you'd also want to assert a starting x/y, then call move, then assert the final x/y so that you can tell those values were actually updated and I don't have to guess where the initial x/y values were.

* You're adding a bit too much logic in all of your tests. You want to call as few methods and set as few properties as possible in your tests so that you can really isolate your assertions to test a single thing. In a test like [this](https://github.com/michaelyons/game-time/blob/master/test/Game-test.js#L233), you're recreating the entire flow of the game. If this test fails, figuring out where it went wrong would be really difficult because you are calling so many methods. You should be able to simply set a player's score to 3 then check that `gameOver` is true.

### JavaScript Style & OOP

* 4 - Application has exceptionally well-factored code with little or no duplication. SRP (single responsibility principle) and DRY (don’t repeat yourself) principles are utilized. There are zero instances where an instructor would recommend taking a different approach. Application is organized into classes (and correctly uses inheritance) and there are no instances where instructor would suggest moving logic or data to another class. The business-logic code driving functionality is cleanly separated from rendering, view-related code.
* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.
* 2 - Your application has a significant amount of duplication and one or more major bugs. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. There are one or more major bugs.
* 1 - Your client-side application does not function. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Application is not separated into classes, or methods and properties are illogically assigned to classes. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Business-side logic and view-related code is not separated at all.

* You should probably have a `Player` class that inherits from the GamePiece, and adds a `trail` property that's made up of `GamePieces`. The trails are currently on your `Game` class, but each trail is specific to a single player - so they should be on a `Player` class instead. Same with each player's score. Those are specific to a player, not the game itself.

* Storing your players in an array would allow you to reduce a lot of repetitive code in places like [this](https://github.com/michaelyons/game-time/blob/master/lib/Game.js#L26) and [this](https://github.com/michaelyons/game-time/blob/master/lib/Game.js#L102-L122). You could `forEach` over them to apply values and call methods on each one.

### Workflow

* 4 - The developer/team effectively uses Git branches and many small, atomic commits that document the evolution of their application with descriptive commit messages. The team displays good pairing practices (driver-navigator, dividing up work, etc) and utilizes some sort of planning tool (GitHub issues, Waffle, Trello, etc). The team develops a clear MVP (minimum viable product) and conducts a DTR (define the relationship). Both members contribute meaningfully to the application.
* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.
* 2 - The developer/team makes large commits covering multiple features that make it difficult for the evaluator to determine the evolution of the application. The team does not utilize a planning tool or equitable pairing practices. One or both members do not contribute meaningfully to the application.
* 1 - The developer/team committed the code to version control in only a few commits. The evaluator cannot determine the evolution of the application.