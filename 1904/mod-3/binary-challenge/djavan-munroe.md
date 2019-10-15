### Evaluator: Travis Rollins
### Students: Djavan Munroe
### Comments:
* Commits could get broken out more.
  * Examples include tests for actions & reducers or all app tests
  * Would help make commits a bit more descriptive as well.
* README is pretty solid.  Would also include wireframes. Would also like to have seen a project management tool used.
* A lot of linter errors (19).  Make sure to add the script `"lint": "eslint src/"` to check it.
* App is a lot of fun.  Great routing (might make the nav buttons a bit bigger)
* Really cool idea to search for pokemon, catch them, and transfer them over to your team.
  * Good detail that the user can only set 6 pokemon on the team.
* Might recommend a loader when searching for next pokemon.
* Love the animated pokemon on the team.  
* Like the subtle animations when a user is clicking a specific pokemon to be moved.
* Would like to see a 404 page if the user goes to a route that doesn't exist.
* Would like to see you do something with the catch in a `try catch`.  Set the error to something. (in App component in componentDidMount)
* No propTypes at all.
* Clean App component and Nav component.
* Good work keeping store pretty clean.  Would like to see an `error` and `loading` property in Redux store as well.
* Actions and reducers are clean and named well.
* Really like the helpers file for cleaning and picking generations.
* Good work using async await in your apiCalls
* addPokemon and removePokemon seem pointless in PC.  Call the method from your props.
* PC component could get broken out into more components since you are having to do multiple maps and it's getting a bit long in the render.
* 38 tests, only one failing is decent but could have more.
* Good work starting tests in SearchForm
  * Would like to see you test catchPokemon in mapDispatchToProps as well.
  * Good work testing handleChange, but missing tests for handleSubmit and handleSurprise
* Missing tests for your helper functions.  This would be a great place to add more tests.
* Good work with testing everything in mapDispatchToProps in SearchForm.
* Good work testing actions and reducers.
* A couple more tests could be added in apiCalls but in general solid work with the ones you have.

## Rubric 

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.
* 4 - The application completes all iterations above and implements one or more of the extensions.  The evaluator has no recommendations for design changes.

### Project Professionalism

* 2 -  README has been updated but is missing group members, setup, tech used, application images, or etc.  Wireframes are included and a project management tool was started, but are not utilized throughout the entire project. Project has more than 5 linter errors. Project team makes large infrequent git commits. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.
* 4 - Functions including fetch calls have been refactored to be reusuable for multiple queries.  Frontend data always matches the backend data.  Data fetched from API is run through a cleaning function (which lives in a separate file).  Implements excellent error handling if server is down or fetch fails.  This includes loading images as well as error messages on the frontend.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.
* 4 - All requirements from 3 met, and no duplication of data exists in the
  store. Data in the store remains flat (not nested).

### Testing

* 2 - Nearly all unit tests are in place. React components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods.  All routes have been tested as well including dynamic routes.  There are tests in place for actions, reducers, mapStateToProps, and mapDispatchToProps.  No attempt to test async functionality was made.
* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
* 4 - React Router components have been refactored for developer empathy and code quality is clean.  Application accounts for undefined routes. UX is excellent and set up well to have links to all routes on all pages.