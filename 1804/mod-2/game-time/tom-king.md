# Game Time
* Students: Tom King
* Evaluator: Brittany Storoz

Comments:
* Nice work going solo, but don't use it as an excuse to do less ;) It's often actually faster and easier working alone than struggling through pairings, so instructors and future employers won't have much sympathy
* Testing was better after re-visiting it, use this project as a way to practice writing tests in the future and finish fleshing them out
* Demonstration of OOP skills is clear though code can be difficult to read at times -- there's a lot of complex logic here, but make sure you can still speak to it after graduation. An employer might ask you to talk through the code and I think you will have a hard time remembering exactly how it works (I would even if I wrote it). Create a branch for yourself with annotations for each line during an intermission/after graduation if you have to. 

### Functional Expectations

* 4 - Application is fully playable and exceeds the expectations set by instructors

* Level up extension in place by adding more missiles, good work!

### User Interface

* 3 - The application has many strong pages/interactions, but a few holes in lesser-used functionality.

* Just needs a bit more instruction on keyboard shortcuts but otherwise easy to understand and play

### Testing

* 3 - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.

* Also [assert](https://github.com/tomkingkong/game-time/blob/master/test/Game-test.js#L31) that it's an instance of the Game class. (Do this for all test classes), there is syntax for that assertion specifically if you look through the mocha chai docs.

* [It should set instance properties appropriately](https://github.com/tomkingkong/game-time/blob/master/test/Game-test.js#L34) not store all the things

* Your descriptions like [this](https://github.com/tomkingkong/game-time/blob/master/test/Game-test.js#L85) are a little vague, and should be more geared towards explaining what the actual code is doing. e.g. "It should decrease the player's missile count when they shoot"

* Do you need to be calling [findBattery](https://github.com/tomkingkong/game-time/blob/master/test/Game-test.js#L129-L131) twice each time? This looks like something that should be refactored so that you can just call it directly in your assertion once.

* [This](https://github.com/tomkingkong/game-time/blob/master/test/Game-test.js#L141) isn't really asserting what you're describing. It looks like you're just testing that the game level gets updated after the loop.

* [I would break out setup like this](https://github.com/tomkingkong/game-time/blob/master/test/Weapon-test.js#L8-L20) into a separate file since you're repeating it across test files, then you can just import it in rather than having it in all those different places. 

### JavaScript Style & OOP

* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.


* If you're just using [this](https://github.com/tomkingkong/game-time/blob/master/lib/Context.js) for tests, a more common convention would be to put it in a directory like `/tests/mocks/Context.js` to separate it from the code that's actually needed to run your application.

* Based on the instance properties on your Game class, it looks like you could make another Player/Enemy class that keeps track of its own missiles and weapon counts.

* `false` is a weird default value for the [nextLevel](https://github.com/tomkingkong/game-time/blob/master/lib/Game.js#L19) property. I'd assume it would be 0, but I also see you have a level property as an integer. Are both of these completely necessary? Can what you're accomplishing with `nextLevel` be done automatically without routing through an instance property?

* With so many instance properties on your Game class, I'd recommend at least ordering them in some semantic order - like keeping all the player/enemy, missile/weapon information together, all the score/level information together, etc.

* Having to call [animateMissiles twice](https://github.com/tomkingkong/game-time/blob/master/lib/Game.js#L33-L34) looks more like a bug than something intentional. I see you're passing different values in for each call, but could you refactor `animateMissiles` to exist on a Player/Enemy class that's shared between the two? That way you could instead call `this.player.animateMissiles()` and `this.enemy.animateMissiles()` which makes the distinction more clear for why you're calling it twice.

* [No](https://github.com/tomkingkong/game-time/blob/master/lib/Game.js#L38-L40). ;) 

* All of these [if elses](https://github.com/tomkingkong/game-time/blob/master/lib/Game.js#L32-L56) are really difficult to read. One way to refactor, if they're all entirely necessary, is break out the logic within each if/else into a separate function with a very descriptive name. Something like:

```js
if (!nextLevel && !gameOver) {
  startGame();

  if (!enemy.missiles.length) {
    advanceToNextLevel();
  }
}

else if (nextLevel) {
  if (timer !==0) {
    continueLevel();
  } else {
    advanceLevel();
  }
}

else if (gameOver) {
  handleGameOver();
}
```

That would make it at least clear what all the different behaviors/routes the game could take based on those conditions.

* Having a [pause](https://github.com/tomkingkong/game-time/blob/master/lib/Game.js#L63) method directly after a `togglePause` method is a little bizarre. I'd rename this to be something like `drawPauseText()`

### Workflow

* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.

* You definitely want more than 76 commits on a project of this size and complexity Aim for about 200 at minimum. This is a sign your commits are probably all doing a bit too much and the diffs are likely not easily readable.

* Look into `git rebase --interactive` for squashing commits. You have a *lot* of commits that have the same exact message, likely as you iterated on whatever piece of functionality you were working on. (Like "Optimize High Score Input"). You don't want duplicate commits like that. You want to merge them into a single commit by squashing.