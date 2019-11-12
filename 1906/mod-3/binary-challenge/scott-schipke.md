### Evaluator: Travis Rollins
### Students: Scott Schipke
### Comments:

**Project Professionalism**
* Great work with number of commits.  Could have more branches.
  * Appreciate descriptive commits and branches being specific.
* Make sure to stick with your GH projects after setting it up.
* Great work with README including setup, tech used, description, and different screenshopts of the app.
  * Would be nice to include wireframes as well.
* Good work only having 4 linter errors.

**Specification Adherence**
* Appreciate the loading icon!
* Really great user experience going through and selecting which options.
* Would be so nice to go back or start over and restart the game (both in the middle of the game or after a team wins).
* Great conditional rendering if a user wins or if it is a tie.

**React Architecture**
* Good work separating apiCalls into separate file. 
  * Love that you are checking that the response is ok before doing `response.json()`
* Great work creating a cleaner function and testing them!
* In your `Form` component, great work using a try catch.  Now remember to do something with the error message.  Set it to state and render it.
  * Good work breaking out methods in the Form and keeping code clean.
* Excellent work including propTypes for all components.
* Remember to move components that are hooked to the store inside of a `containers` directory.

**Redux Architecture**
* Could be nice to keep track of `isLoading` and `errorMsg` in the store.
* Great work keeping track of necessary props like currentTeam, currentQuestion, and all of the questions in an array.
  * A little but if duplicate data being held both in questions and for the currentQuestion.  Maybe give them each a unique id?
* Actions and reducers look solid.
  * Appreciate you are only passing a payload when necessary.

**Routing**

*Update*
* Good work implementing routes
* Could be nice to have dynamic routing for each of the questions.
* Would be nice to have a button to take the user back to the start of the app.

**Testing**
* Excellent number of tests.  Most I had this mod.
* Excellent work testing your actions and reducers.
* Good work having multiple tests for different snapshots in your `App`.
  * Good work testing mapStateToProps.
* Great testing in your Form component including testing that async functions were called.
  * I also appreciate the tests for changes in state and simulating events.
* Great work testing your helper functions.
* Great work with testing the `Board` as well including `mapStateToProps` and `mapDispatchToProps`
* Great work testing your isolated fetch.
  * Remember to also have another sad path test if the promise rejects (like if the server is down).

## Rubric 

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.
* 4 - Functions including fetch calls have been refactored to be reusuable for multiple queries.  Frontend data always matches the backend data.  Data fetched from API is run through a cleaning function (which lives in a separate file).  Implements excellent error handling if server is down or fetch fails.  This includes loading images as well as error messages on the frontend.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.

### Testing

* 4 - All async functionality is tested.   Asynchronous tests cover happy paths as well as multiple sad paths.  All pieces of functionality have been tested and are passing and run efficiently (using mount only when appropriate). Evaluator has no recommendations for testing.

### Routing

* 2 - Application uses React Router, but does not display the appropriate components upon navigating.  There are one or more issues with the UX and access to routes is either unclear or not full implemented on some pages.
* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.