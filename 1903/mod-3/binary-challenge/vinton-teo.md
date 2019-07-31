### Evaluator: Travis Rollins
### Students: Vinton Te'o
### Comments:
* Good number of commits and breaking them out into smaller pieces
  * Good consistency with commit messages
* Would like to see more PRs and branches
* Good work with README
* Cheers for adding propTypes
* Nice work with 404 page
* Would have liked to see some dynamic routing.
* Nice work with no linter errors.
* What is the reasoning behind having all maps in the store?
* Only need to be displaying one.  Should not be in store and in state of `ShowCase` component
* Instead of firing multiple actions in the Form on lines 54-56, fire one action and pass multiple arguments.
* Nice loading screen
* Store is pretty flat otherwise, no duplicated data
  - Might store spartan, emblem, stats, etc. in one part of the reducer
* Would be consistent with async/await or using .then
* Good work testing actions & reducers as well as apiCalls
* In `App.test.js`, would like to see more properties in the mockState to make sure that mapStateToProps returns an object you expect to get.
* Great tests in form testing for changes in state and events

## Rubric

### Specification Adherence

* 3 - The application uses the above technologies to a professional level. The evaluator has minimal recommendations for refactoring or design changes.

### Project Professionalism

* 3 - PropType functionality is complete, the codebase has less than 5 linter errors, README has been updated with all group members. Project utilized wireframes from the outset. All git commits are atomic, made first to branches, and use descriptive and concise commit messages. Project demonstrates a fundamental understanding of React architecture.

### Testing

* 4 - All requirements from 3 met, all async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.
* 2 - At least one component is not connected with Redux appropriately. Application state is mutated by more than just Redux. The Redux store is missing application data that it should be handling.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
