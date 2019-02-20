# Game Time
* Students: Tim Taylor
* Evaluator: Pam

Comments:
* UX is good - easy to move through the game; buttons are appropriately disabled throughout. UI could use some tightening up in the following areas: font is small, making it hard to read; inputs aren't lined up with buttons; use modals instead of alerts
* Small bug past round 1: would not allow me to pick a letter that is part of the answer... resulting in a lost turn;
* Super excited that you went above and beyond when given the extension on your project - nice work!

*Given extension until 2/8 at 5PM to improve in areas of functionality, and OOP. Scores reflect changes made with extension given*

### Functional Expectations

* [x] Proficient - Application is fully playable and meets all requirements of the spec.

### User Interface

* [x] Proficient - The application has many strong pages/interactions, but a few holes in lesser-used functionality.

### Testing

* [x] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.

* Be sure that you aren't forcing your testing to do things that your application doesn't do naturally. (Here)[https://github.com/timmiller601/gametime-wheel-of-fortune/blob/master/test/test-Game.js#L57 ] you are essentially doing what the first expression already does in `findPuzzles` and then running `findPuzzles`. For this test - the output is the 4 puzzles for the game with the caveat that each puzzle for each round has a different number of words. To test that, it would look something like this:

```js
  it.('should return four puzzles from the dataset with a varying number of words', function() {
    const foundPuzzles = game.findPuzzles();
    
    expect(foundPuzzles).to.have.length(4);
    expect(foundPuzzles[0]).to.have.property('number_of_words', 1);
    expect(foundPuzzles[1]).to.have.property('number_of_words', 2);
    expect(foundPuzzles[2]).to.have.property('number_of_words', 3);
    expect(foundPuzzles[3]).to.have.property('number_of_words', 4);
  });
```

* Try to think of testing as a way of isolating parts of your Game. I would expect to see a new instance of Player being created in (this `beforeEach`)[https://github.com/timmiller601/gametime-wheel-of-fortune/blob/master/test/test-Player.js#L9-L11 ] block for our Player Game tests


### JavaScript Style & OOP

* [x] Proficient - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.

* Good job with naming methods!
* Not sure why an object called `wheelObj` is being passed to the constructor (here)[https://github.com/timmiller601/gametime-wheel-of-fortune/blob/master/src/Wheel.js#L4 ]
* Nice small methods in Game - generally, most of the code is pretty easy to step through and read.
* Some opportunities for refactoring and moving functionality around.

### Workflow
* [x] Proficient - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.