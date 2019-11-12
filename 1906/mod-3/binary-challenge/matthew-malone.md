### Evaluator: Travis Rollins
### Students: Matthew Malone
### Comments:

**Project Professionalism**
* Good number of commits and start to branches.
  * Good work being consistent with descriptive commits and branches
* Excellent work using a project management tool.
  * I appreciate how you broke the tickets out into multiple pieces.
* Great work with the README including the table of contents, mission, useability of the app, and screenshot.  Might include wireframes as well.
* A very large amount of linter errors.
  * Don't need to include an `.eslintrc` file.  React already has it's own linter.  This is likely a result of this.

**Specification Adherence**
* Really awesome idea here.
  * Smooth experience and has a deep meaning to it.
* Would be nice to have the ability to restart the game. (seems like this is a future iteration in the MVP)
* Really good work with the UI
* Appreciate having the indicator when two words do not match.

**React Architecture**
* Remember to clean up commented out lines like in the `completedCard`
* Good work keeping components and containers in their respective directories.
* Gets a bit div heavy in card components.
* Extremely confusing to have methods defined inside of `componentDidMount` (and much more challenging to test)
  * Separate the methods out of the `componentDidMount`.
* Completely missing propTypes.
* No reason to have `Game` as a class component.  Keep it functional.
* Quite a lot going on in `round` component with some of the methods.
  * Could be interesting to see how this could get refactored.
  * Good work keeping logic out of render.
* Remember to do something with errors.  Console.logs are not helpful.

**Redux Architecture**
* Gets a bit nested with the gameData property.
  * An array of arrays can be a bit tricky to utilize.  Maybe could be refactored a bit.
* Love the setup of `prefixRoundData` and `prefixMeaningData` and matching ids as necessary.
* Would like to see an `errorMsg` and `isLoading` property if something breaks or takes a long time to load.
* I believe the hardcoded data in `gameData` used in actions is unnecessary.
* Otherwise good work with actions and reducers.
  * Would love to hear an explanation of the `.sort((a, b) => 0.5 - Math.random())` used in some of the reducers.
* Good work using `mapStateToProps` and `mapDispatchToProps` where necessary.
  * `Round` component appears to be having quite a few extra props that no longer exist.  Clean this up.

**Routing**
* Buttons and clear and routing is smooth.  
* Could be nice to log out and go back to the previous page if I wanted to change my name.
* Good work using `component` for Routes since you didn't need to pass props
* Would be awesome to look into creating a 404 page if a route doesn't exist.

**Testing**
* Missing a lot of tests.
* Good work with having most snapshot tests.
* Good work testing out your actions and reducers.
* Good work testing mapDispatchToProps in `WelcomeForm`.  Missing tests for mapStateToProps here.
  * Would also be good to have some unit tests for methods and checking changes in state.
* Good start with testing apiCall for url and happy path.
  * Include tests for sad path.
* Alot of mock data like in the `App` that could be included in a separate file and used in multiple files.
* No tests for event simulations, changes in state, or mapStateToProps.
  * Also missing tests for async methods as well as regular methods.

*Update*
* Great work including some tests for the sad path!
  * I think for the `server down` test, it might be better to have the `Promise.reject` as opposed to resolve.  When a 500 error happens, it rejects throwing an error object.
* Good work testing `mapStateToProps` in your App.
  * I would say to take this one step further, add in all of the properties that should be in the store.  Then the expect is after running the function, it should only return the `gameData`.
* Good work with the first test for the event simulation in `WelcomeForm`.  Super close on the 2nd one.  Double check the error (it is because you are missing some props).  `setPlayer is not a function` because you haven't passed it that prop.
  * Good example of the state change as well in `WelcomeForm`.
* Double check some of the warnings you are getting.  Some of these are coming from the App.  As a result, tests are silently failing.
  * `Cannot read property 'word' of undefined`
  * `addFetchedWords is not a function`

## Rubric 

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.
* 4 - The application completes all iterations above and implements one or more of the extensions.  The evaluator has no recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 2 - PropType functionality is complete.  There are no unnecessary props being passed down to child components.  However, there are still methods that are being created inside of functional components instead of being passed down through props from a class component.  File structure is modular but api calls have not been broken out into a separate file.  
* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Redux Architecture

* 2 - At least one component is not connected with Redux appropriately. Application state is mutated by more than just Redux. The Redux store is missing application data that it should be handling.
* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.

### Testing

* 2 - Nearly all unit tests are in place. React components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods.  All routes have been tested as well including dynamic routes.  There are tests in place for actions, reducers, mapStateToProps, and mapDispatchToProps.  No attempt to test async functionality was made.
* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Routing

* 2 - Application uses React Router, but does not display the appropriate components upon navigating.  There are one or more issues with the UX and access to routes is either unclear or not full implemented on some pages.
* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.