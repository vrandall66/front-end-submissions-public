### Evaluator: Travis Rollins
### Students: Emily Dittmer
### Comments:
* Would like to see more commits and breaking them out into smaller pieces
  * Such as breaking out commits for tests
* Nice work creating some issues and creating a README
* Good work with propTypes, missing a few like propTypes for mapDispatchToProps
* Missing tests for mapStateToProps on `SuggestionContainer`
* A few linter errors not including tests
* Nice work including a 404 page
* A little too similar to MovieTracker still
* Having multiple scrolls (page scroll and then card scroll) can create a bad UX 
  * Might recommend being able to click each card so they can view the full synopsis
* Some duplicate data in store
  * Storing the entire object in the `watchList` property as opposed to storing the show or movie's id
* Good work handling routes, would have liked to see dynamic routing.
* Great work testing actions, reducers, apiCalls
* Good tests for mapStateToProps and mapDispatchToProps but missing tests for the methods, mocking events, etc. for `SuggestionCard`
  * Missing component tests for `Watchlist` as well
* `SuggestionCard` does not need to be a class component since it is not using the constructor.

## Rubric

### Specification Adherence

* 3 - The application uses the above technologies to a professional level. The evaluator has minimal recommendations for refactoring or design changes.

### Project Professionalism

* 3 - PropType functionality is complete, the codebase has less than 5 linter errors, README has been updated with all group members. Project utilized wireframes from the outset. All git commits are atomic, made first to branches, and use descriptive and concise commit messages. Project demonstrates a fundamental understanding of React architecture.
* 2 - Project is missing PropTypes, README updates, wireframes, or has more than 5 linter errors. Project team makes large infrequent git commits. Project shows a basic understanding of React.

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.
* 2 - Nearly all unit tests for Redux and React are in place. No attempt to test async functionality was made.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 4 - All requirements from 3 met, and always chooses the correct component for rendering, as well as the correct Route API. Application should account for undefined routes.
