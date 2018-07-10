# Game Time
* Students: Laura and Alex
* Evaluator: Brittany Storoz

Comments:
* Both articulated their knowledge of classes/OOP very well
* Little too many things in the index.js that could be moved into the Game class but overall classes seemed well-structured and they each had appropriate methods and instance properties on them

### Functional Expectations

* 3.5 - Application is fully playable without crashes or bugs

* Attempted an extension but didn't quite get there

### User Interface

* 3.5 - The application is pleasant, logical, and easy to use. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer. Couple stylistic things that could improve.

* Able to use the application without any guidance or instruction
* Make a bit more difference in the green of the frog vs. the grass so I can tell I've been killed and have started over
* Prioritize the game by giving it a bit more space, and de-emphasize the instructions/about section by making it more of a sidebar

### Testing

* 3 - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.

* You also want to assert that your objects are instances of the class [they belong to](https://github.com/Alexbruce1/game-time/blob/master/test/Vehicle-test.js#L26). You can import `expect` from chai and test something like: `expect(vehicle).to.be.an.instanceof(Vehicle);`

* Nice pre-and-post [assertions here](https://github.com/Alexbruce1/game-time/blob/master/test/Frog-test.js#L77-L83)

* [This test](https://github.com/Alexbruce1/game-time/blob/master/test/Frog-test.js#L97) makes me feel like `generateScore` is something that should happen automatically every time the frog moves, rather than having to call it manually after each `move` call. 

* In order to test Game methods like `drawBackground` and `loadStartScreen`, you'd want to mock out that `ctx` object so that they don't yell at you. In your setup code, like in a `before` block, you could do something like: 

```js
  const ctx = {
    fillRect() => {}
    otherMethods() => {}
  }
```


### JavaScript Style & OOP

* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.

* Stylistic nitpick, decide whether youre using [single quotes or double quotes](https://github.com/Alexbruce1/game-time/blob/master/lib/Game.js#L19-L20)

* [These](https://github.com/Alexbruce1/game-time/blob/master/lib/Frog.js#L6-L9) instance properties should be passed into super and inherited from the parent, not set here.

* [Score](https://github.com/Alexbruce1/game-time/blob/master/lib/Frog.js#L11) is something I might put on the game class rather than the frog.

* [These](https://github.com/Alexbruce1/game-time/blob/master/lib/Frog.js#L46) might be a bit too complex for ternaries. Keep them as simple and bare bones as possible, and if you can't, switch to an if else

* Seems like [this](https://github.com/Alexbruce1/game-time/blob/master/lib/Frog.js#L82) else condition is unecessary if you're just setting the pre-existing value equal to itself.

### Workflow

* 3.5 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.

* Nice readable and consistent commit messages

* Try not to commit [commented out code](https://github.com/Alexbruce1/game-time/commit/dde097221ec3b65ca3eca234ef1258515547c18e), you can always delete it entirely and then go back to a previous commit to retrieve it again if you need it!