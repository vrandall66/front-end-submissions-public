### Evaluator: Travis Rollins
### Students: Zoë Ketcham-Harvey
### Comments:

**Project Professionalism**
* Excellent number of commits
  * Would like to see more branches in the future even on solo projects.
* Great work using an issue.  Could use more in the future.
* Missing wireframes and project tool management (yes they are still helpful even when working by yourself.)
  * Otherwise good work including summary, tech used, and images of app in README.
* Great work having no linter errors!!!

**Specification Adherence**
* Good work displaying a lot of data on the page.
* Still some styling could be included for people's personal pages and favorites page.
* Able to have duplicates for favorites.
  * Would be nice to at some point.
  * Could be also nice once on favorites, to click on a person and bring up their stat info again.
* Quite a number of errors including propType failures and an onClick getting an object type instead of a function.

**React Architecture**
* Make sure to do something with errors instead of returning them in the catch.  Then render them.
* Shouldn't need to give a key on components in the routes in `App`.
* A lot of conditionals in the `RosterContainer`.  Potentially update that/clean it after fetching it so you don't have to do that in this component.
* Some repeated methods included like `getSingleRoster` both in the App and TeamCard.
  * So how you could pass this method down.
* Make sure to check if the response is ok before doing `response.json()` in your apiCalls.
* A lot of refactoring could happen in the `NavLogos` component.  Create the array somewhere and then map through it.
* Good work including propTypes for all components. (including props from the store)

**Redux Architecture**
* Some pieces of data could be cleaned so it doesn't all exist in the store.
  * For example, the favorites page is displaying only the name, but in the store there are many other properties being included as well.
* Good work including isLoading and errorMsg properties in the store.
* Actions and reducers are set up well.
* Remember to use actions like `isLoading` and `hasErrored` when necessary.
  * This includes state like the `errorMsg`.  Some unnecessary props being passed to components that aren't needed.
* Remember to move components hooked to the store inside of a `containers` directory.

**Routing**
* Would recommend moving navigation links to the top instead of the bottom so it is easy to see/access.
  * Good work making all routes accessible.
* Potentially might set up the routes to be more dynamic.
  * For example, if I want to see a specific player, use a route like `/player/:id` and use the id to find which one to display.
* Look into how you can create a 404 page if a route doesn't exist.

**Testing**
* Great number of tests.
  * Good work testing out actions and reducers. (including different scenarios depending on the type of action)
* Need some work with apiCall tests.
  * Look into your mockResponse.  Because they are empty objects, the tests are failing due to there being no properties in them for it return. (such as `stats` or `dates`)
  * Also missing sad path tests.
* Good work testing `mapDispatchToProps` for App.
  * Again would like to see a bit more than an empty object in many scenarios.
  * Don't forget to include `errorMsg` in your mockState for `mapStateToProps` in App.test.js.
* Good snapshot tests.
* Missing tests for event simulations and methods.  (both regular methods like `cleanUpPlayer` in component and async methods)

*Update*
* Appreciate the test for simulating an event for handleDetails.
* Good work including some tests for mapStateToProps and mapDispatchToProps.
* Made improvements with apiCall tests but still running into errors like `TypeError: Cannot read property '0' of undefined` or `Unhandled promise rejection`.
* Good work for including some sad path tests.
* Good work testing `componentDidMount` and check for change in state in mouseEnter.


## Rubric 

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.
* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 2 - PropType functionality is complete.  There are no unnecessary props being passed down to child components.  However, there are still methods that are being created inside of functional components instead of being passed down through props from a class component.  File structure is modular but api calls have not been broken out into a separate file.  

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.

### Testing

* 2 - Nearly all unit tests are in place. React components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods.  All routes have been tested as well including dynamic routes.  There are tests in place for actions, reducers, mapStateToProps, and mapDispatchToProps.  No attempt to test async functionality was made.
* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
* 4 - React Router components have been refactored for developer empathy and code quality is clean.  Application accounts for undefined routes. UX is excellent and set up well to have links to all routes on all pages.