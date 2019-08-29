### Evaluator: Travis Rollins
### Students: Brianna DelValle
### Comments:
* Really nice styling on your app, UI is very clean
  * Good highlighting of the active class for the navigation links.
  * Routes are always solid and accessible.
  * Text on scrolling crawl could be a bit bigger.
  * Nice work with the loading message
* Would keep looking into how you can create a 404 page if a user goes to a route that doesn't exist. (I know you started working on this)
  * aka `localhost:3000/yolo`
* Typically would recommend starting default state to what it will be after fetch
  * Example: planets and people will be an array after the fetch.  So start them as empty arrays
  * This makes it a bit easier so you don't have as much conditional logic like in the `CardContainer`
* Unless you are displaying multiple errors on the same page, I would recommend only having one piece of state for errors.
  * Regardless of whether or not it is a people or vehicle error, the error is only being shown once on that route.
* Nice work separating your fetches
  * Don't need to assign it in the constructor `this.fetchMovie = fetchMovie`.  You can call `fetchMovie` in your App.
* With the idea of `updateAppState`, I think it's fine to call setState where needed.  This makes it easier to test, but I don't recommend testing the `componentDidMount` aside from checking that a method has been called.
* How could you refactor the `Route` components?
  * Could use an array prototype method similar to how you did in the `CardContainer`
  * Could create a dynamic route and use the `match` prop that is given to us in the render
* Nice work breaking out helper functions into their own files
  * Including helper functions for `Card` and `Fetch`
  * Could separate fetches and cleaner functions into their own files as well. 
* Good work breaking out fetches based on responsibility
  * Really like the reusability of `fetchCards`
  * Would recommend not moving the function that `setsState` into the fetch file.  Return the data back from the function, and call `setState` still in the component.
  * Solid work handling errors with `.catch()`
  * Would have another check to see if `response.ok` is true before doing `response.json()`
* Think about how you could refactor the Card component
  * Instead of having to write out all of the data and importing all the possible props, try using something like `Object.keys` on your props.  Based on that, map through and return the data you need.
* Great work including your propTypes
* Instead of including the `Adapter for enzyme` in all of your tests, insert it into a `setUpTest.js`
  * Only need one Adapter for it to work for all tests
* Good work including snapshot tests for all types of data (as seen in `Card.test.js`)
* Really nice testing in your App.test.js
  * Great work testing changes in state with methods
  * Good use of `async/await`
  * Shouldn't need to find the component for route testing.
    * Running something like `expect(CardContainer).toHaveLength(1)` is perfectly fine as well.
    * I really like the test route test for `/favorites`.  Could clean up the setState since the only thing that the favoritesContainer is dependant one is the favorites in state.
* Continue to keep working on testing for fetches in `Fetch.test.js`
  * Write a test for if the correct url or options are passed as an argument.
  * Write two sad path tests (one for if the piece of data doesn't exist, and another for if the server is down)
    * If the promise.resolves, but the property of ok is false, it should give one error
    * If it hits a catch, the promise will reject, giving a different error
* Would like to see more commits.  This was a big project, and several could get broken out more. [example](https://github.com/bld010/swapibox/commit/2e91a7de6c211687209c7dcc2cc427c444b07974)
  * Same with branches
* Really nice work on your README
* Only 4 linter errors, good work!
* Would recommend including wireframes as well as project board in your README as well.
* Nice work using a rebase workflow!  



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

### Testing

* 3 - A valid attempt to test asynchronous functionality has been made.  Asynchronous tests cover happy paths as well as multiple sad paths.
* 4 - All async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).  Unit tests for snapshots and methods cover not only happy paths but also sad paths.  Evaluator has no recommendations for testing.