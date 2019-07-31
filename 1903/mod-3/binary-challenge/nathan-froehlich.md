### Evaluator: Travis Rollins
### Students: Nathan Froehlich
### Comments:
* Good work with README
* Good work with number of commits and breaking them out into smaller pieces
  * Good consistency with commit messages
* Nice work with no linter errors.
* Make sure to add node-sass to your dependencies so it doesn't break when running on another computer.
* Good work with 404 page
* Would be nice to have some kind of loading indicator 
  * For example when I click Facts, it takes a while for the data to fetch.  Having a loader would help make sure I don't think the app froze.
* Could be helpful when getting types of jokes, to have some kind of drop down since the user maybe not know what other types of jokes there are aside from `random`.
* Redux store is really flat, great work with no duplicated data!
* In `Advice` container, shouldn't need a check for the event on line 30 in handleSubmit
* Good work separating out logic
* mapDispatchToProps looks a bit strange.  Shouldn't need to be doing async/await
  * Fetch the data beforehand, then pass the data through when calling the action.
  * Either that, or utilize thunks.
* Would recommend adding more to your mockStore in the `Advice.test.js` to make sure that mapStateToProps returns the object you expect to get
* Shouldn't need to create another method called getFact in the `Facts` container.
  * Call the `getRandomFact` method on the click of the button
* Good work separating out reducers & testing reducers/actions
* Clean up comments in apiCalls file.  Also clean up console.logs in other files.
  * Nice job using the switch statement for handling your apiCalls
* Be consistent with capitalizing etc.  The reducers directory doesn't need to be capitalized. Same for ApiCalls.  Leave components capitalize but the rest is fine with camelCase.


## Rubric

### Specification Adherence

* 3 - The application uses the above technologies to a professional level. The evaluator has minimal recommendations for refactoring or design changes.

### Project Professionalism

* 4 - All requirements from 3 met, codebase has zero linter errors/warnings and readme contains screenshots of application. Project team uses a rebase workflow, taking advantage of github issues to track work. Project shows a complete mastery of React architecture.
* 3 - PropType functionality is complete, the codebase has less than 5 linter errors, README has been updated with all group members. Project utilized wireframes from the outset. All git commits are atomic, made first to branches, and use descriptive and concise commit messages. Project demonstrates a fundamental understanding of React architecture.

### Testing

* 4 - All requirements from 3 met, all async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).

### Redux Architecture

* 4 - All requirements from 3 met, and no duplication of data exists in the store. Data in the store remains flat (not nested).
* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 4 - All requirements from 3 met, and always chooses the correct component for rendering, as well as the correct Route API. Application should account for undefined routes.
