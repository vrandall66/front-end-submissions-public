### Evaluator: Travis Rollins
### Students: Sam Freeman
### Comments:
* Great number of commits and good, detailed commit messages.
* Good work on your README as well including images of the App and wireframes
* Would have liked to seen you use a project management tool
* Excellent work having no linter errors.
* Excellent route handling, good work with the style of the app as well.
  * A bit challenging to find the home page unless the user clicks on search and click `Show Popular` games.
* Would like to see some kind of message if I don't own any games or have any favorites.
* Fun functionality with searching for a random game
* Also very cool that a user can download the rules to a game.
* I'd play around with the styling more of the details page,  focusing on how to organize a page with a lot of data.
* Would like a loading screen.
* Would take a look at how you can build out a 404 page
* Great work on actions & reducers
* Good work with separating fetches into apiCalls
  * Would prefer that you do something with the error.  Console.logging error is not helpful.
* Missing propTypes
* Overall clean code, very readable.  Good work breaking out components.
* Great number of tests.  Exciting that there was only one failing test! (snapshot needed to be updated)
* Good work testing changes in state, snapshots, event simulations, apiCalls, actions, reducers, & testing mapStateToProps & mapDispatchToProps

## Rubric 

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 
* 4 - Codebase has zero linter errors/warnings and README is well documented with images of different pages, setup, purpose of application, and group members. Project team uses a rebase workflow, taking advantage of github issues to track work.

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.
  store. Data in the store remains flat (not nested).

### Testing

* 4 - All async functionality is tested.   Asynchronous tests cover happy paths as well as multiple sad paths.  All pieces of functionality have been tested and are passing and run efficiently (using mount only when appropriate). Evaluator has no recommendations for testing.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
* 4 - React Router components have been refactored for developer empathy and code quality is clean.  Application accounts for undefined routes. UX is excellent and set up well to have links to all routes on all pages.