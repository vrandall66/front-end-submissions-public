### Evaluator: Travis Rollins
### Students: Ann Cerveny
### Comments:
* Commits can definitely get broken out more.  Not enough commits or branches.
  * This will help in making commits more descriptive as well.
* Would have liked to see a project management tool.
* No README or wireframes.  (Sounds like you did use wireframes and a project management tool, remember to include some pics of it inside your README)
* Good work with having only 2 linter errors.
* Fun survey to pick a team!  Some issues with styling where things aren't being contained well.
* Questionaire is broken when trying to select either option.
* Good work separating file structure into components and containers.  Multiple files that are containers that haven't been moved to the containers directory yet though.
* Good work implementing propTypes.
* How could NFLPick and NCAAPick get refactored into one?
* Good work separating apiCalls into their own file.
* Good start with tests, it looks like a few snapshots need to be updated.
  * Good work implementing reducer tests.
  * Missing many action tests.
  * Good work simulating events in `PickALeague`.  Would like to see some tests on the methods `getNFLTeams` and `getNCAATeams`.  
    * Same for `PickMatchUp`, test out the methods that are in there.  
  * Good tests for mapStateToProps and mapDispatchToProps.

## Rubric 

### Specification Adherence

* 1 - The application is missing multiple features outlined above and in it's current state is non-functioning. Developer did minimal to no CSS for this project.
* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.

### Project Professionalism

* 1 - Either the README is incomplete, wireframes are not used, no project managment system was utilized, or more than 10 linter errors are present. Git history does not show evolution of project with many large and inconsistent commits. 

### React Architecture

* 2 - PropType functionality is complete.  There are no unnecessary props being passed down to child components.  However, there are still methods that are being created inside of functional components instead of being passed down through props from a class component.  File structure is modular but api calls have not been broken out into a separate file.  
* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.
* 4 - All requirements from 3 met, and no duplication of data exists in the
  store. Data in the store remains flat (not nested).

### Testing

* 2 - Nearly all unit tests are in place. React components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods.  All routes have been tested as well including dynamic routes.  There are tests in place for actions, reducers, mapStateToProps, and mapDispatchToProps.  No attempt to test async functionality was made.
* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Routing

* 2 - Application uses React Router, but does not display the appropriate components upon navigating.  There are one or more issues with the UX and access to routes is either unclear or not full implemented on some pages.
* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.