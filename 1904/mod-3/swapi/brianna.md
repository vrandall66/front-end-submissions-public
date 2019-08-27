### Evaluator:
### Students:
### Comments:

## SwapiBox Rubric

### Specification Adherence

* 1 - The application is missing multiple features outlined above and in it's current state is non-functioning. Developer did minimal to no CSS for this project.
* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.
* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.
* 4 - The application completes all iterations above and implements one or more of the extensions.  The evaluator has no recommendations for design changes.

### Project Professionalism

* 1 - Either the README is incomplete, wireframes are not used, no project managment system was utilized, or more than 10 linter errors are present. Git history does not show evolution of project with many large and inconsistent commits. 
* 2 -  README has been updated but is missing group members, setup, tech used, application images, or etc.  Wireframes are included and a project management tool was started, but are not utilized throughout the entire project. Project has more than 5 linter errors. Project team makes large infrequent git commits. 
* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 
* 4 - Codebase has zero linter errors/warnings and README is well documented with images of different pages, setup, purpose of application, and group members. Project team uses a rebase workflow, taking advantage of github issues to track work.

### React Architecture

* 1 - PropTypes are substantially unused. Project shows little understanding of React and significant refactoring is required including but not limited to component structure, knowing when to use class vs functional components, mutation of props, or etc.  Unneccessary data is being passed down to child components through props. File structure is not modular.
* 2 - PropType functionality is complete.  There are no unnecessary props being passed down to child components.  However, there are still methods that are being created inside of functional components instead of being passed down through props from a class component.  File structure is modular but api calls have not been broken out into a separate file.  
* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.
* 4 - Functions including fetch calls have been refactored to be reusuable for multiple queries.  Frontend data always matches the backend data.  Data fetched from API is run through a cleaning function (which lives in a separate file).  Implements excellent error handling if server is down or fetch fails.  This includes loading images as well as error messages on the frontend.

### Routing

* 1 - Application uses React Router, but does not render/use all routes according to spec. Application does not utilize built in React Router components and manipulates history instead.  UX is challenging and frustrating where multiple pages on the application are missing links to routes.
* 2 - Application uses React Router, but does not display the appropriate components upon navigating.  There are one or more issues with the UX and access to routes is either unclear or not full implemented on some pages.
* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
* 4 - React Router components have been refactored for developer empathy and code quality is clean.  Application accounts for undefined routes. UX is excellent and set up well to have links to all routes on all pages.

### Testing

* 1 - There is little or no evidence of testing in the application.  There are some UI tests including snapshot tests, but major gaps in unit testing functionality.
* 2 - Nearly all unit tests are in place. Components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods (including `componentDidMount`).  No attempt to test async functionality was made.
* 3 - A valid attempt to test asynchronous functionality has been made.  Asynchronous tests cover happy paths as well as multiple sad paths.
* 4 - All async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).  Unit tests for snapshots and methods cover not only happy paths but also sad paths.  Evaluator has no recommendations for testing.