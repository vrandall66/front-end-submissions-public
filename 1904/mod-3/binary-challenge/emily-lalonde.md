### Evaluator: Robbie
### Students: Emily
### Comments:

* Good to see dynamics routing! Typically the route `http://localhost:3000/home/1432` would be something more like `http://localhost:3000/breweries/1432` to denote that `1432` is a specific brewery out of all the breweries
* **Bug:** I am seeing my notes for a brewery on every brewery
* Cool to see that you got a google map going! A next step is to get info windows going for each marker to display the brewery name
* I think on desktop the top menu can remain expanded instead of the hamburger
* For routing, no need to have a separate route for `http://localhost:3000/name-search/2408`. This could also be `http://localhost:3000/breweries/2408` from wherever the user comes from (search or the home page) - That way, some of the dynamics routes can be eliminated

* **20% of tests are failing at the time of review** Need to fix these

## Rubric 

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.
  store. Data in the store remains flat (not nested).

### Testing

* 2 - Nearly all unit tests are in place. React components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods.  All routes have been tested as well including dynamic routes.  There are tests in place for actions, reducers, mapStateToProps, and mapDispatchToProps.  No attempt to test async functionality was made.
* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Routing

* 2 - Application uses React Router, but does not display the appropriate components upon navigating.  There are one or more issues with the UX and access to routes is either unclear or not full implemented on some pages.
* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
