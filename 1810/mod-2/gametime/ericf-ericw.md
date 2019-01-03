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

* 2 - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. Tests that are written are often ineffective/not testing the right code.


* For your player class tests, you should be setting up a new instance of a Player, not your entire Game. This is another one of those core benefits of OOP is that every class should be so independent and isolated from each other that you don't need to spin up the entire app in order to test a small piece of functionality. e.g. [this test](https://github.com/ericweissman/wheel_of_fortune/blob/master/test/Player-test.js#L61-L62) is still manually forcing something to be true (the player's name) and testing the code you just wrote in your test file, rather than letting your app take over and testing the code in your app. You would need to rewrite this test to be something like:

```js
let bob = new Player('bob');
expect(bob.name).to.equal('bob');
```

The game should be completely removed from this test file. Any instance of `game.players[0]` should be replaced with something like `bob`. `buyVowel` method isn't tested, 'LOSE A TURN' isn't tested (we should be checking if the player's `turn` property has changed from `true` to `false`).

* Puzzle tests are mostly missing, and the one you do have isn't assertive enough -- we would want to make sure the function is actually returning something that *looks* like what we want. Not just that the two return something different. e.g. assert that you actually get an object back that has the properties a puzzle should have.

* [Here](https://github.com/ericweissman/wheel_of_fortune/blob/master/test/Game-test.js#L59) and [here](https://github.com/ericweissman/wheel_of_fortune/blob/master/test/Game-test.js#L52) are more examples of where you are writing code for the sake of a test and then testing *that* code rather than your app. Don't manually force the game's wheel value or puzzle value to change. Let the app do that when and where it's supposed to. Your Game class generates a wheel and puzzle value for itsel the second it's instantiated, so they should already be properties on the instance of your game that you created in your test file. There's no need to manually change them. Just call the method you're trying to test and make sure you have a new wheel and new puzzle.

* Overall I'm really concerned with the level of understanding for testing. This is something you should get some individualized pairings on going forward as there are some serious fundamental misconceptions I'm noticing here. Reaching out 2 hours before the project is due to get help on testing is not the time to do so.



### JavaScript Style & OOP

* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.

* Overall the separation of logic between your classes looks good, the right classes are taking care of the right behaviors/properties. (Save some of the update score logic that's in the game class and should be moved to the players)

* What does [this](https://github.com/ericweissman/wheel_of_fortune/blob/master/Game.js#L7) property represent? Based on the name it doesn't sound like it would be an array, though the default value of an empty array tells me otherwise...

* [Here](https://github.com/ericweissman/wheel_of_fortune/blob/master/Game.js#L46-L48) I would just automatically set `this.wheel` to a new instance of a wheel rather than setting it to a variable first (the variable isn't helping you much there, and actually looks a little more confusing because you're just calling it `newWheel = new Wheel`). I would say you could have the wheel call it's own `generateValues` method immediately in the constructor rather than having to invoke it here. That way you can get rid of that last line as well.

### Workflow

* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.


* Mostly nice, consistent commit messages except for capitalization -- make sure your messages always start with a capital letter
* Generally a nice breakout of your commits, where they're not doing too much, but make sure that only relevant changesets make it into each commit. e.g. based on [this](https://github.com/ericweissman/wheel_of_fortune/commit/54bd8f08f81d177cacf93cf548672e3971272aba) commit message, I would expect that the index.html changes wouldn't be included there. That kind of change should go in a subsequent commit.
* You might want to look into `git squash` to merge some commits before you push them into master -- just a nice tool to be aware of. You can reduce duplicate commits (I noticed a couple) that do the same thing like 'Update README' (if you do this 5 times you can just squash it into a single commit when you're done that includes all the changes you made over all those commits)
