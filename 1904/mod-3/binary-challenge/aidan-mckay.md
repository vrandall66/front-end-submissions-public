### Evaluator: Travis Rollins
### Students: Aidan McKay
### Comments:
* Good number of commits but would like to see more branches.
* Good work with README including setup, description, and images.  Would also like to see pictures of wireframes ( I know you made them).
* Would also like to have seen you use a project management tool.
* Great work having no linter errors.  To use the linter in your package.json, include the script `"lint": "eslint src/"` inside of your package.json.  Then run `npm run lint`.
* Love the UI and design.  Some parts with spacing could be addressed.
  * Header could get shrunk a bit.  Might add more spacing between filter options.
* Store is pretty empty aside from events.  Would like to have seen maybe error, loading icon, or filters in there as well.
* Would look into how you can create a 404 page if route doesn't exist.
* Remember to include a `try/catch` in your componentDidMount in App.  If something breaks, then you can do something with the error.
  * Good work with try/catch in your `Search`.
* Good work including propTypes!
* Great work with tests, a few that are silently failing.  Check the errors you are getting with the apiCalls.   Also getting some warnings on propTypes in your tests.
  * Good work at testing all of your apiCalls, cheers!
  * Good tests for the actions and reducers that you have.
  * Excellent work testing that async methods have been called in methods and `componentDidMount`
  * Good tests for mapStateToProps and mapDispatchToProps
  * Also good tests for simulating events and checking changes in state.

## Rubric 

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 2 -  README has been updated but is missing group members, setup, tech used, application images, or etc.  Wireframes are included and a project management tool was started, but are not utilized throughout the entire project. Project has more than 5 linter errors. Project team makes large infrequent git commits. 
* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 4 - Functions including fetch calls have been refactored to be reusuable for multiple queries.  Frontend data always matches the backend data.  Data fetched from API is run through a cleaning function (which lives in a separate file).  Implements excellent error handling if server is down or fetch fails.  This includes loading images as well as error messages on the frontend.

### Redux Architecture

* 1 - Application state is mostly outside the control of Redux. Application did not make use of Redux actions and reducers to mutate state. Components do not demonstrate a clear understanding of stateful vs. statelessness.
* 2 - At least one component is not connected with Redux appropriately. Application state is mutated by more than just Redux. The Redux store is missing application data that it should be handling.

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.
* 4 - All async functionality is tested.   Asynchronous tests cover happy paths as well as multiple sad paths.  All pieces of functionality have been tested and are passing and run efficiently (using mount only when appropriate). Evaluator has no recommendations for testing.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.