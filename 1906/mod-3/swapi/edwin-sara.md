### Evaluator: Robbie
### Students: Edwin and Sara
### Comments:

* The opening form is great! Really like the hover lightsaber effect - careful with red because it can signal that something is wrong
* Great job on all of the features!
* The color coding for the movie series is a nice touch
* Like that the top bar doesn't take up a lot of space - a bit squished, but I like it

* Good job breaking up your apiCalls into smaller functions
* For `getCharacters`, `.then(response => response.characters).then(response => response.splice(0, 10))` the second `.then()` could be brought into the first (use multiple lines, it's ok!)
* The routes look good in your app - no redundant routes that I see (tell me more about the `<Redirect to='/' />` for each route)
* Great job with the form - super clean and simple

* 32 tests written - getting a lot of `Received promise rejected instead of resolved Rejected to value: [TypeError: response.json is not a function]` warnings in console
* Great tests overall, very thorough
* For the `'should call the handleFavorite prop when the favorite button is clicked'` test, be sure to interrogate what is passed into the functions you expect to be called. Yes, they were called, but were they called with the correct information?

* Nice job with the kanban board (good job using columns as progress tracking instead of features)


## SwapiBox Rubric

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and concise commit messages. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.
* 4 - Functions including fetch calls have been refactored to be reusuable for multiple queries.  Frontend data always matches the backend data.  Data fetched from API is run through a cleaning function (which lives in a separate file).  Implements excellent error handling if server is down or fetch fails.  This includes loading images as well as error messages on the frontend.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
* 4 - React Router components have been refactored for developer empathy and code quality is clean.  Application accounts for undefined routes. UX is excellent and set up well to have links to all routes on all pages.

### Testing

* 3 - A valid attempt to test asynchronous functionality has been made.  Asynchronous tests cover happy paths as well as multiple sad paths.
* 4 - All async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).  Unit tests for snapshots and methods cover not only happy paths but also sad paths.  Evaluator has no recommendations for testing.