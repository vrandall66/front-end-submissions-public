### Evaluator: Travis Rollins
### Students: Katherine Williams
### Comments:
* Good number of commits, but almost no branches.  Remember to start on a different branch even when working by yourself.
  * Good detailed commit messages.
* Excellent work sticking with using your GH Projects
* Excellent work with README including setup, description, and images.
* Good work having no linter errors.
* Good work including a loading image while it gets data.
* Noticed that styling doesn't take the full page (white space on the right side).
* Like the listing of national parks and monumnents.
  * Many of the national monuments/other break due to it not finding the latLong.
  * Need some conditional logic so it doesn't entirely break.
* Good dyanmic routing of national parks.  Would look at why image cannot be found. Clean UI though and appreciate being able to return back to the list.
  * For favoriting, would recommend having some styling on the button so when I click it, I know that it has been favorited.
  * Currently I am able to favorite a place multiple times.  I shouldn't be able to remove a favorite if it hasn't been favorited yet.
* Excellent work including a 404 page!!!!
* Some duplicate data in store.  Shouldn't need to store the entire object into the favorites array.  That already exists elsewhere.  Find a way to store just the ID.  Otherwise good work with actions and reducers!
* Good work breaking out fetch calls into apiCalls file.
* Excellent work separating components and containers.
* Cheers to including propTypes!
* Good work setting error message to state in App component and rendering it.  
* Good number of tests, but almost a 1/4th of them are either skipped or failing.
  * Note that you can't test changes in state on a functional component.
  * I understand many that are skipped are tests on routing.  No worries, testing router with Redux store is very challenging.
* Good work with tests for apiCalls, actions, reducers, mapDispatchToProps, mapStateToProps
  * Good work testing simulation events in `Park` component.
  * Missing some tests on methods and changes in state like in App (`filterAndStoreParks`)

## Rubric 

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.

### Project Professionalism

* 2 -  README has been updated but is missing group members, setup, tech used, application images, or etc.  Wireframes are included and a project management tool was started, but are not utilized throughout the entire project. Project has more than 5 linter errors. Project team makes large infrequent git commits. 
* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.
* 4 - Functions including fetch calls have been refactored to be reusuable for multiple queries.  Frontend data always matches the backend data.  Data fetched from API is run through a cleaning function (which lives in a separate file).  Implements excellent error handling if server is down or fetch fails.  This includes loading images as well as error messages on the frontend.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Routing

* 4 - React Router components have been refactored for developer empathy and code quality is clean.  Application accounts for undefined routes. UX is excellent and set up well to have links to all routes on all pages.