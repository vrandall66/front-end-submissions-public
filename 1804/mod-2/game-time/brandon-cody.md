# Game Time
* Students: Brandon & Cody
* Evaluator: Pam Lovett

### Functional Expectations

* 3 - Application is fully playable without crashes or bugs

- Nice job with no bugs or broken functionality.

### User Interface

* 3 - The application has many strong pages/interactions, but a few holes in lesser-used functionality.

- Missing some playability features: no clear indication that the game has restarted when all lives are lost; no win/loss screen; missing multiple levels of difficulty

### Testing

* 2 - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.

- ESLint showing more than 10 complaints
- Many of the tests could be combined so as not to be so granular - Ex: All the default states that you are testing in Frog could be combined into a single test that states `('it should have default states')`
- Remove empty index files
- A lot of the tests are not actually testing for what is described in the `it` block. This is true of almost all of the tests in `Game-test.js`. Ex: In `Game-test.js` we have the following:
`it('should create an empty array of logs')` with the following expectation:
`expect(game.logs).to.be.an('array')` 
This is not actually testing for the array to be empty. Instead, it should read: 
`expect(game.logs).to.deep.equal([])`
- Add tests for collision functionality


### JavaScript Style & OOP

* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.

- Unclear why you have separate classes for `Lives` and `Score`. These could both be tracked as properties under the `Game` class



### Workflow

* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.

- Good amount of commits. Remember to follow conventions for commits (first letter capitalized, be descriptive but concise, use subject line for up to 50 characters and add more detailed info in the body, explain the `what` and `why` of the commit in your body)
- Stop doing commits like `generate hella logs`, `pushing`, and `this will work`