### Evaluator: Robbie
### Students: Lacy and Jessie
### Comments:

* The home screen is intense! Caught me off guard at first, but I like it
* Small bug in the form: if you select a rank and then switch back to "Choose", then you are still able to submit the form
* Bug: filling out the form does not let me move on...
* Do not see any way to favorite
* Clicking Favorites page link is not going anywhere
* I like the overall dark theme - it's simple and clean

* Be consistent by moving `App` and it's other files into a `App` directory like the other components
* Why multiple `Switch` components in `App`? A switch can handle multiple routes within it
* Nice job breaking out functions for apiCalls
* In apiCalls, `getHomeworld(homeworld).then(world => world)`, the `.then()` is probably not necessary since you are just passing the same value through to another promise

* 10 tests written, but only 5 passing at time of eval - **this needs to be worked on for a passing project** Thursday at 5pm

## SwapiBox Rubric

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Routing

* 2 - Application uses React Router, but does not display the appropriate components upon navigating.  There are one or more issues with the UX and access to routes is either unclear or not full implemented on some pages.
* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.

### Testing

* 2 - Nearly all unit tests are in place. Components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods (including `componentDidMount`).  No attempt to test async functionality was made.
