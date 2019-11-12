### Evaluator: Travis Rollins
### Students: Lacy Rudd
### Comments:

**Project Professionalism**
* Excellent number of commits and good start with branches.
  * Nice work keeping branches and commits descriptive
* Great work using your GH Projects including labels and staying up to date with what is completed, what you are working on, and what is left to do.
* Excellent work including several issues that need to be worked on as well.
* Nice work with README including description, focuses, wireframes, screenshots, and setup.  Cheers!
* Double check linting warnings (about 6 of them).  Remember to include `"lint": "eslint src/"` in your package.json under the scripts object and run `npm run lint` in terminal.

**Specification Adherence**
* Really cool to be able to pick a different date and display the different asteroids.
  * Nice that I can click a link to explore more data.
* Overall app is very dark.  Between dark pictures and dark elements that I can click, can be challenging to make out UI.  
  * Might be interesting to run through an accessiblity reader.
* React Router is mainly non-existant.  No routes are setup except for NavLink.  

**React Architecture**
* Great work implementing try/catch for methods like in `App`.
* Good work breaking out apiCalls into their own files and checking if the response is okay before trying to do `response.json`.
* Some good conditional rendering in the `AsteroidContainer`
  * Could use some refactoring though to make it a bit cleaner.
* Good work breaking out functions into helper file.  Could you explain one of these functions?
* Appreciate the cleanNeoData function but it is a monstrous function.
  * Could this get refactored or use something other than reduce?
* Missing propTypes.

**Redux Architecture**
* Good work of keeping track of loading and errorMsgs in the global store.
* Appreciate the rendering of the errorMsg.
* Good work keeping store flat without duplicate data.
* Great work setting up your actions and reducers.
* Do not need `mapStateToProps` in the AsteroidCard component since it is getting its props from it's parent.

**Routing**
* Routing currently is not implemented aside from the one `NavLink`.

*Update*
* Now has routes for asteroids and APOD.
* Works as expected and takes the user to both routes.
* Routes are always accessible.
* Look into how you can create a 404 page if a route doesn't exist.

**Testing**
* Good work testing actions and reducers.
* Great work testing out the apiCalls including all paths.
  * For testing if a server is down, I would still have fetch return a Promise but have it reject with the specific error.
* Good work having all snapshot tests in.
* Need to see some tests for `mapStateToProps` and `mapDispatchToProps`.
  * Would like to see some tests for methods in App like did async methods/actions fire.
  * Would love to see an event simulation test to check that the `displayDateSelectedNeos` method was called when clicking on the button on `AsteroidDateCard`.

*Update*
* Great work testing your `mapStateToProps` and `mapDispatchToProps` in your App
* Great work including some event simulation tests.
* A couple of apiCalls still silently failing such as `Cannot read property 'url' of undefined`.  

## Rubric 

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.
* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 2 - PropType functionality is complete.  There are no unnecessary props being passed down to child components.  However, there are still methods that are being created inside of functional components instead of being passed down through props from a class component.  File structure is modular but api calls have not been broken out into a separate file.  
* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Redux Architecture

* 2 - At least one component is not connected with Redux appropriately. Application state is mutated by more than just Redux. The Redux store is missing application data that it should be handling.
* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.
* 4 - All async functionality is tested.   Asynchronous tests cover happy paths as well as multiple sad paths.  All pieces of functionality have been tested and are passing and run efficiently (using mount only when appropriate). Evaluator has no recommendations for testing.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
