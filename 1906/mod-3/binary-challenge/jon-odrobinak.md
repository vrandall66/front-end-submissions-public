### Evaluator: Travis Rollins
### Students: Jon O'Drobinak
### Comments:

**Project Professionalism**
* Massive commit especially in the beginning.  Not enough commits.
  * Continue to keep making more branches as well in the future.
  * Commits and the few branches that are there are descriptive
* Started GH project but almost no flow on it right now except for the one card.
* I appreciate a couple of the issues that have been included.
* Good work with README including overview, how to get started, tech used, and images.
  * Would also like to see wireframes included as well.
* Good work only having 3 linter errors.

**Specification Adherence**
* Would recommend disabling the Search button until all inputs are filled.
  * Not a great experience including longitude and latitude.
  * Strange to have button and search link.
  * After putting in the exact pieces of data, I've got the schoolList and number of them but doesn't display until after clicking the next button.  I would have both happen at the same time.
* Think UX would have been better without the Form and focus the audience on just one location like it is set up.
* Styling is a bit rough.  Would be nice to have cards display all locations.

**React Architecture**
* Good work with implementing catches in the Form, make sure to set the `error.message` to state.
* A lot of unnecessary props used in the `SchoolCard` component.
* Good work implementing propTypes.
* Some refactoring could happen in the `SchoolContainer`.  Don't need the test data.
  * Remember to also separate `SchoolCard` and `SchoolContainer` into separate directories.
* apiCalls look solid.  Good work checking if `response` is not okay.

**Redux Architecture**
* I appreciate `errorMsg` and `isLoading` properties being kept track in store.
* `schools` property is a little nested.  Likely could separate the properties but not too bad.
* getAllSchools action and reducer are not used.  Would clean up commented out code in the future.
* Actions and reducers look good.
* Some unnecessary props being passed from store to the component like in `App` with schools and error props not being used.
  * Same for SchoolCard, don't need `mapStateToProps`
  * Don't need all of the store passed into `mapStateToProps` for SchoolCardContainer.  Just schools and `error if you render it`.
  * Only using mapDispatchToProps once.

**Routing**
* ExtraDetails route doesn't work as a result of not using the `match` object to utilize params and display the correct information.
* Dynamic routing is there though.  Appreciate being able to go back to home route.
* Would be nice if it cleared out the store as well.

**Testing**
* Missing tests for actions.
* Some tests for reducers which look good.
  * Still missing reducer tests for `errorMsg` and `isLoading`.
* Good work testing apiCall method `getSchoolDetails`.
  * Write up the tests for `fetchAllSchools` as well.
* Make sure snapshot test for Form is up to date.
* Great work simulating events and testing changes in state on the `Form` component.
  * Also good work testing the `mapDispatchToProps` here as well.
* Good work testing mapStateToProps

## Rubric 

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.

### Project Professionalism

* 2 -  README has been updated but is missing group members, setup, tech used, application images, or etc.  Wireframes are included and a project management tool was started, but are not utilized throughout the entire project. Project has more than 5 linter errors. Project team makes large infrequent git commits. 

### React Architecture

* 2 - PropType functionality is complete.  There are no unnecessary props being passed down to child components.  However, there are still methods that are being created inside of functional components instead of being passed down through props from a class component.  File structure is modular but api calls have not been broken out into a separate file.  
* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Redux Architecture

* 1 - Application state is mostly outside the control of Redux. Application did not make use of Redux actions and reducers to mutate state. Components do not demonstrate a clear understanding of stateful vs. statelessness.
* 2 - At least one component is not connected with Redux appropriately. Application state is mutated by more than just Redux. The Redux store is missing application data that it should be handling.

### Testing

* 2 - Nearly all unit tests are in place. React components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods.  All routes have been tested as well including dynamic routes.  There are tests in place for actions, reducers, mapStateToProps, and mapDispatchToProps.  No attempt to test async functionality was made.
* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Routing

* 2 - Application uses React Router, but does not display the appropriate components upon navigating.  There are one or more issues with the UX and access to routes is either unclear or not full implemented on some pages.