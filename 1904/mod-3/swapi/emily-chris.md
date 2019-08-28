### Evaluator: Robbie
### Students: Emily and Chris
### Comments:

* The intro game is so cool! I was looking for the scrolling text, but this was a fun surprise.
* Quite a bit of unused space on the index pages before you click on a particular card
* How do I unfavorite something?...seems like this is not working yet given the commented-out test
* I like the overall theme of the card glow, matched the Star Wars logo glow
* Bump up the opacity of the cards a little bit so the background is not quite as distracting

* Good job extracting your fetch calls from the App component - it would be great to move those "cleaner" methods to a helper file too so they don't clutter up the App component file
* Instead of using the `header` element, use the `nav` element to contain navigation elements: https://github.com/CLLane/swapi-box/blob/master/src/App/App.js#L161
* Consider how to make these base routes iterable, could you iterate through a list of routes and render the routes according to the list instead of hard-coding each base route? https://github.com/CLLane/swapi-box/blob/master/src/App/App.js#L212
* Good job getting the dynamic routing going for each type
* Consider how to refactor this so you don't have to list everything going into the Card component? https://github.com/CLLane/swapi-box/blob/master/src/Container/Container.js#L12-L26 Could you reduce the props or spread the props?
* Since these are all `h4` elements, could you iterate through the list of data to dynamically create these elements instead of hardcoding each of them? https://github.com/CLLane/swapi-box/blob/master/src/Card/Card.js#L14-L22
* Why pass the whole card info into `addToFavorites` in App?

* Great job getting async testing into your project
* A few linting warnings remaining
* One failing snapshot test at time of review
* For this test, it would be good make sure this still works when there are multiple people in the `people` array in state: https://github.com/CLLane/swapi-box/blob/master/src/App/App.test.js#L89 Do you know it is finding the correct person or is it just finding the correct thing because it is the only one? 
* Be sure to test that `toggleFav` has been called with the correct arguments that you expect: https://github.com/CLLane/swapi-box/blob/master/src/Card/Card.test.js#L67


## SwapiBox Rubric

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 
* 4 - Codebase has zero linter errors/warnings and README is well documented with images of different pages, setup, purpose of application, and group members. Project team uses a rebase workflow, taking advantage of github issues to track work.

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.
* 4 - Functions including fetch calls have been refactored to be reusuable for multiple queries.  Frontend data always matches the backend data.  Data fetched from API is run through a cleaning function (which lives in a separate file).  Implements excellent error handling if server is down or fetch fails.  This includes loading images as well as error messages on the frontend.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
* 4 - React Router components have been refactored for developer empathy and code quality is clean.  Application accounts for undefined routes. UX is excellent and set up well to have links to all routes on all pages.

### Testing

* 1 - There is little or no evidence of testing in the application.  There are some UI tests including snapshot tests, but major gaps in unit testing functionality.
* 2 - Nearly all unit tests are in place. Components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods (including `componentDidMount`).  No attempt to test async functionality was made.
* 3 - A valid attempt to test asynchronous functionality has been made.  Asynchronous tests cover happy paths as well as multiple sad paths.
* 4 - All async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).  Unit tests for snapshots and methods cover not only happy paths but also sad paths.  Evaluator has no recommendations for testing.