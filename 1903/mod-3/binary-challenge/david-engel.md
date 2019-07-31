### Evaluator: Travis Rollins
### Students: David Engel
### Comments:
* Good amount of commits
  * Some commits for tests could be broken out a little more
  * Good consistency with commit messages
* Good amount of PRs and nice README
* Cool idea getting user and their weight to show how much they would weigh on a planet
* Nice work, no linter errors
* Good work with the store, no duplicate data
* Nice work with the loading image while waiting for data to be fetched.
* Love that you mapped through the Routes to clean up code for your `MainDisplay`
  * Potentially one step further to refactor could be using a dynamic route.  `/:planet/` or `/status/:planet`
* Missing container tests for `MainDisplay` for mapStateToProps
* Would like to see extra properties added to mockState on line 35 in `App.test.js` to make sure that you are getting back properties you would expect.
  * Also missing the properties of loading & error.
* Good tests for actions/reducers
* Good work separating out a cleaner file for cleaning your data for each planet.
* Would clean up `StatsForm` component a little bit.
  * Likely could create a couple more components and separate logic out more
* Missing a 404 page of route doesn't exist

## Rubric

### Specification Adherence

* 3 - The application uses the above technologies to a professional level. The evaluator has minimal recommendations for refactoring or design changes.

### Project Professionalism

* 3 - PropType functionality is complete, the codebase has less than 5 linter errors, README has been updated with all group members. Project utilized wireframes from the outset. All git commits are atomic, made first to branches, and use descriptive and concise commit messages. Project demonstrates a fundamental understanding of React architecture.

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Redux Architecture

* 4 - All requirements from 3 met, and no duplication of data exists in the store. Data in the store remains flat (not nested).
* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
