# Game Time
* Students: Andrew & Joel
* Evaluator: Brittany

Comments:
* Wonderful TDD, strongest effort I've seen there in a while
* Good file structure and organization, nice clean github commit history -- although be sure to be consistent with capitalization and the tense of your commit messages. Couple discrepencies there.

### Functional Expectations

* 4 - Application is fully playable without crashes or bugs

### User Interface

* 3.5 - The application has many strong pages/interactions, solid effort put into UI.


* The IDs [here](https://github.com/andrew-t-james/game-time/blob/master/index.html#L12-L17) should be on the p tags, rather than the spans -- IDs help to group related content. You could change your selectors in JS/CSS to access `#score span` 

### Testing

* 4 - Project has a running test suite that exercises the application at multiple levels. The test suite covers almost all aspects of the application and uses mocks and stubs when appropriate.

* (Only thing I would mention is doing that refactoring to use the before/beforeEach hooks for repetitive setup code


### JavaScript Style

* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.

* Calling the same function [twice in a row](https://github.com/andrew-t-james/game-time/blob/master/lib/index.js#L34-L35) looks more like a bug than something intentional. I'd refactor whatever's happening in here into two separate functions with different names or add functionality to the existing function so you can call it just once.

* [This](https://github.com/andrew-t-james/game-time/blob/master/lib/Frogger.js#L22-L28) is a good candidate for using a ternary rather than an if/else statement:

```js
const frogIsOnLog = // all that logic to determine this value;
this.floating = frogIsOnLog ? true :  false;
```

### Application Organization

* 4 - Application is organized into classes (and correctly uses inheritance) and there are no instances where instructor would suggest moving logic or data to another class. The business-logic code driving functionality is cleanly separated from rendering, view-related code.

### Workflow

* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.