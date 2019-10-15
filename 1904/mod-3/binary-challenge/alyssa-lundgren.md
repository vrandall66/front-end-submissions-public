### Evaluator: Travis Rollins
### Students: Alyssa Lundgren
### Comments:
* Great number of commits, a few that could be a bit more detailed such as `Remove extras from App`, but in general I thought messages were super clear on what you worked on.
* Good work sticking with using GH Project
* Great work with your README, I would also include your wireframes.
* Decent work with linter.  Only 6 linter errors.
* Such a cool idea for an application.  Clean UI.  
  * Wonder if in a future iteration, the user could select multiple options in the survey?
* Love the Masonry layout, noticed that most of them are on the left side (scrolls forever).  Might keep working on the layout.
* Would be cool to select products and do something with them. (aka dynamic routing or put them into a cart)
* Good work with routing, would look into how you can create a 404 page.
* Appreciate error handling and loading icon!
* Very clean Redux store, excellent work with actions & reducers.
* Good work separating cleanerData as well as testing them!
* Good work separating components and containers.
* Excellent work implementing propTypes!  Hooray!
* Good work keeping all components functional.
  * Careful of having too many functions in functional components.  Makes testing them very difficult.  Hence why the tests you wrote for your `Nav` weren't passing.
* Good work with number of tests and only having one breaking.
  * Appreciate tests for actions, reducers, cleanerFiles, apiCalls, mapStateToProps, & mapDispatchToProps
    * Would recommend breaking out reducer tests into separate files.
  * Want more component tests.  Lacking a lot of tests like in the Quiz on methods and changes in state.  (review testing your methods and setting them to mock functions)

## Rubric 

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.
* 4 - The application completes all iterations above and implements one or more of the extensions.  The evaluator has no recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 4 - Functions including fetch calls have been refactored to be reusuable for multiple queries.  Frontend data always matches the backend data.  Data fetched from API is run through a cleaning function (which lives in a separate file).  Implements excellent error handling if server is down or fetch fails.  This includes loading images as well as error messages on the frontend.

### Redux Architecture

* 4 - All requirements from 3 met, and no duplication of data exists in the
  store. Data in the store remains flat (not nested).

### Testing

* 2 - Nearly all unit tests are in place. React components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods.  All routes have been tested as well including dynamic routes.  There are tests in place for actions, reducers, mapStateToProps, and mapDispatchToProps.  No attempt to test async functionality was made.
* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
* 4 - React Router components have been refactored for developer empathy and code quality is clean.  Application accounts for undefined routes. UX is excellent and set up well to have links to all routes on all pages.