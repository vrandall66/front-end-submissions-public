# Game Time
* Students: David and Liz
* Evaluator: Pam

Comments:
* Nice README. If you haven't already, I would deploy this on GitHub pages.
* Excellent UI/UX - simple, pleasant, and easy to follow - simple things to tighten up (disable the button before play, correct camel casing on categories)
* Opportunities for refactoring JS and getting rid of some duplication across classes.

### Functional Expectations

* [x] Proficient - Application is fully playable and meets all requirements of the spec.

### User Interface

* [x] Exceptional -  Meets all expectations for `Proficient`. In addition, the application is pleasant, logical, and easy to use. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer.

### Testing

* [x] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.

* Good job with importing spies for use at top of the file. Opportunities for filling gaps in testing. 
(This it block)[https://github.com/easbell/Jeopardy/blob/master/test/Clue-test.js#L12-L33 ] is an example of some of the common gaps found in testing suite. Mock data can live outside of your `describe` block (so all tests have access to it). You'll want to have a block that tests for default properties ofas well as blocks that test for your method (including the conditional logic within it). Something like below:

```js
var mock = {
  question: "What MTV plays 24 hours a day",
  pointValue: 100,
  answer: "music videos",
  categoryId: 10
};

var correctAnswer = "Music Videos";
var incorrectAnswer = "The television";

describe('Clue', function() {
  let game;
  let clue;

  beforeEach(function(){
    game = new Game();
    game.gatherPlayers('jim', 'bob', 'jill');
    clue = new Clue(mock.question, mock.pointValue, mock.answer, mock.categoryId);
  });

  it('should be an instance of Clue', function() {
    expect(clue).to.be.an.instanceof(Clue);
  });

  it('should have default properties', function() {
    expect(clue.question).to.equal('What MTV plays 24 hours a day');
    expect(clue.pointValue).to.equal(100);
    expect(clue.answer).to.equal('music videos');
    expect(clue.categoryId).to.equal(10);
  });

  it('should increase the current player\'s score with a correct answer', function() {
    expect(game.currentPlayer.score).to.equal(0);
    
    clue.correctAnswer(game, correctAnswer);
    
    expect(game.currentPlayer.score).to.equal(100);
    expect(domUpdates.hidePopUp).to.have.been.called(1);
  })

  it('should decrease the current player\'s score with an incorrect answer', function() {
    expect(game.currentPlayer.score).to.equal(0);

    clue.correctAnswer(game, incorrectAnswer);

    expect(game.currentPlayer.score).to.equal(-100);
    expect(domUpdates.changePrompt).to.have.been.called(1);
    expect(domUpdates.changePrompt).to.have.been.called.with('music videos');
  });
});

```

### JavaScript Style & OOP

* [x] Proficient - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.

* Still not sold on extending for `RoundThree` from the `Clue` class, especially considering the similarities between `RoundThree` and `DailyDouble`.
* Opportunities for naming - be sure to name methods by the "action" they are completing. Names make it hard to follow what methods do
* `Game` is doing quite a bit of lifting and keeping track of things unrelated to `Game`, particularly given the other classes (for instance - Game is tracking 3 properties concerning `Round` which are also being tracked by the `Round` class itself). 
  
### Workflow

* [x] Proficient - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.
