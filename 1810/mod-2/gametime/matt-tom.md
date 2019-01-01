# Game Time
* Students: Matt & Tom
* Evaluator: Brittany


### Functional Expectations

* 2 - Application has some missing functionality but no crashes

* Changes make it so that we can only immediately play the bonus round and not fully through the entire game

### User Interface

* 3 - The application has many strong pages/interactions, but a few holes in lesser-used functionality.

* The user flow/interactions are easy to follow which is most important. I would clean up the design a bit by making it a little less busy -- less textures and patterns and differentiate on the colors a bit. Margins & paddings can be cleaned up as well but these are all easy fixes that don't necessarily take away from the intuitiveness of the app.

### Testing

* 2 - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and some of them are out of place

* DailyDouble should also test that any inherited properties from the parent got set appropriately. I want to say you should be testing this `collectWager` method as well but it looks like you also have a `collectWagers` method elsewhere in your codebase and it's difficult to tell what's actually being used or not.

* [These two tests](https://github.com/foxwellm/Jeopardy/blob/master/tests/Question-test.js#L19-L27) seem irrelevant to the Question class -- you're not calling any methods or verifying any properties that a question would care about. These seem more like player tests. It seems like what you're trying to test here is the verifyAnswer method, in which case you would write a test that looks more like this:

```
it should call game.rightAnswer when the guess is correct
  expect(game.rightAnswer).to.have.been.called(1);

it should call game.wrongAnswer when the guess is incorrect
  expect(game.wrongAnswer).to.have.been.called(1);
```

The actual functionality of `rightAnswer` and `wrongAnswer` would then be tested in your Game-test file since those are both methods of your Game class.

* In all test files, you can combine the assertions for default property values like [these](https://github.com/foxwellm/Jeopardy/blob/master/tests/player-test.js#L19-L30) into a single it block.

* Sometimes with tests like [this](https://github.com/foxwellm/Jeopardy/blob/master/tests/player-test.js#L15-L18) you first want to assert that the score was 0 to begin with. Just in case any other test or code had manipulated the starting score ahead of time. Something like:

```
expect(score).to.equal(0);
player.updateScore(100)
expect(score).to.equal(100)
```
   


### JavaScript Style & OOP


* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.

* I'd be curious how [this](https://github.com/foxwellm/Jeopardy/blob/master/JS/DailyDouble.js#L15) is working if you're not passing in an `event` parameter to the method...

* Usually it's more helpful to order your parameters from most commonly included to least commonly included. e.g. [here](https://github.com/foxwellm/Jeopardy/blob/master/JS/Player.js#L2) you are likely always going to be passing in a 'name' value (or at least more frequently than you'd ever pass in `human` or `score`), so this should be the first parameter listed and passed in. That way you can easily omit the other two without worrying about messing up the order of your arguments.

* Your question class shouldn't have to know about the current round or question set. Just it's own properties that tell us what the current question, answer and point values are. You have a lot of instance properties on this class that look redundant. What's the difference between `questionBoxId`, `manipulatedQuestionObj`, `currentQuestion`, etc.? Try to slim this down a bit. You only want to store the absolute bare minimum information necessary for your methods on the class to work. It doesn't look like your question class is using half of the properties you've set on it.

* Most of the functionality in your Game class looks solid, though there are many opportunities for refactoring and cleaning it up to make it a bit more readable. (Most notably in the right/wrong answer methods).

### Workflow

* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.

* Git commit messages are a bit vague and often inconsistent style-wise (e.g you should be writing things like 'Add feature x' not just 'feature added.')
* I'd like to see commits like [this](https://github.com/foxwellm/Jeopardy/commit/5a6ff6fc05f4184de071c2d7abb8c85894f80aa2) be a bit smaller. It looks like the code changes in here are mostly all relevant, but try to find ways to break up this functionality into multiple commits -- maybe the first commit is just creating the DailyDouble class, but it's not being utilized anywhere. The second commit could be stubbing out the properties and methods it might have. The third commit could be instantiating a new one that doesn't actually do anything just yet. Fourth one could be adding the fully integrated functionality.
